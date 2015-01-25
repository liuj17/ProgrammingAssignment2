# ProgrammingAssignment2-Coursera
makeCacheMatrix<-function(x=matrix()){
  s<-NULL
  set<-function(y){
    x<<-y
    s<<-NULL
  }
  get<-function() x
  setsolve<-function(solve) s<<-solve
  getsolve<-function() s
  }  
}

cacheSolve<-function(x,...){
  s<-x$getsolve()
  if(!is.null(s)){
    message("getting cashed data")
    return(s)
  }
  data<-x$get()
  s<-solve(data,...)
  x$setsolve(s)
  s
}
