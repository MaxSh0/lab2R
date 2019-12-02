library("Rglpk")
library("slam")

#задача линейного программирования (1)
obj <- c(10, 14, 12)
mat <- matrix(c(2, 1, 7, 4, 4, 8, 4, 6, 5, 6, 5, 7), nrow = 4)
dir <- c("<=", "<=", "<=","<=")
rhs <- c(120, 280, 240, 360)
max <- TRUE
Rglpk_solve_LP(obj, mat, dir, rhs, max = max)


#транспортная задача
m = 3
n = 4
costs = matrix(c(2,3,4,3,5,3,1,2,4,1,4,2), ncol = n, byrow=TRUE)
direction = c("min", "max")
row.signs=c("=","=","=")
col.signs=c("=","=","=","=")
row.rhs=c(90,60,150)
col.rhs=c(120,40,60,80)

library("lpSolve")
mysolution = lp.transport (costs, "min", row.signs,row.rhs, col.signs, col.rhs)
summary(mysolution)
mysolution$solution
mysolution$objval
