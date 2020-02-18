# repositorio_TIG
Repositorio para aprender a analizar cambios y comentarlos
## 4.3. Compara vectores ####
gasolina <- c(1.357, 1.4, 1.5, 1.25, 1.3, 1.2)
diesel <- c(1.2, 1.1, 1.3, 1.15, 1.2, 1.8)
#A
gasolina>1.4
#B
gasolina>diesel
#C
diesel<=1.2
#Matriz de precio
precio <- matrix(c(gasolina, diesel), nrow = 2, byrow = TRUE)
precio==1.3
precio<=1.3
#Uso de tail, AND y OR
tail(diesel>1.5|diesel<1.2, n=1)
(precio>1.2&precio<=1.5)[,6] #Para gasolina y diesel

(precio[1,6])>(precio[2,6])
which(precio>=1.3) #Posicion donde el precio es mayor a 1.3
precio #ATENCION el orden es por columnas
extremos <- gasolina>1.35
extremos
## 4.4 Genera sentencias condicionales
precio1 = 1.7
if(precio1> 1.5)
print("¡El precio es muy caro!")
precio2 = 1
if(precio2> 1.5){
print("¡El precio es muy caro!")
}else if (precio2<1.2){print("es una ganga")
}else{print("puedes repostar")}
## 4.4 Generar bucle while ####
xx <- 1
while(xx<1.7){
#Esta creciendo el precio de XX y parara en 1.70
xx <- xx+0.1}
xx
##4.5 Bucles for ####
ttt<- matrix (c("O",NA, "X", NA, "O", NA, "X", "O", "X"),ncol = 3)

ttt
for (i in 1:nrow(ttt)){
for (j in 1:ncol(ttt)){
print(ttt[i,j])}}
i <- 0
cnt <- 0
j <- 1
for(x in ttt)
{i <- i+1
cnt <- cnt+1
if(i>3){i=1}
if(cnt>3&cnt<6){j=2}else if(cnt>6){j=3}
print(paste("En la fila",i,"y en la columna",j,"el valor es", x))}