# Kotlin EX-2

## Exercicio 1
```
fun main() {
    val a = 5
    val b = 2
    println(a - b)
}
```

## Exercicio 2
```
fun main() {
    val nome = readLine()
    val sobrenome = readLine()
    
    println("$nome $sobrenome")
}

```

## Exercicio 3
```
fun main() {
    val num1 = 2
    val num2 = 2
    
    println("operação = ${num1 + num2}, ${num1 * num2}, ${num1 - num2}, ${num1 / num2}")
       
  
}

```

## Exercicio 4
```
fun main() {
    val lado1 = 3
    val lado2 = 2
    
    var area = lado1 * lado2
    print(area)
  
}
```



## Exercicio 5
```
fun main() {
    val base = 5
    val altura = 6
    
    var area = ((base * altura) /2)
    print(area)
  
}

```

## Exercicio 6
```
fun main() {
    val peso = 70.0
    val altura = 1.70
    
    var IMC = (peso / (altura * altura))
    print(IMC)
  
}

```

## Exercicio 7
```
fun main(){
    var idadeEmDias = readln().toInt()
    
    if(idadeEmDias > 30){
    var meses = (idadeEmDias / 30).toInt()
    var diasRestantes = idadeEmDias % 30
        if(meses > 12){
        var anos = (meses / 12).toInt()
        var mesesRestantes = meses % 12
            if(anos > 0){
        println("Você é $anos ano(s) $mesesRestantes mês(es) e $diasRestantes dia(s) de idade")
        }
        } else {
            println("Você é $meses meses e $diasRestantes dia(s) de idade")
        }
    } else {
        println("Você é $idadeEmDias dia(s) de idade")
    }
    
}

```
## Exercicio 8
```
fun main() {
    val nota1 = 5
    val nota2 = 8
    val nota3 = 10
    
    var média = ((nota1 + nota2 + nota3) /3)
    print(média)
}

```

## Exercicio 9
```
fun main() {
    var segundos = readln().toInt()

    var horas = segundos / 3600
    var minutos = (segundos % 3600) / 60
    var segundosRestantes = segundos % 60

    println("O evento tem duração de $horas hora(s), $minutos minuto(s) e $segundosRestantes segundo(s).")
}

```

## Exercicio 10
```
import kotlin.math.pow
import kotlin.math.sqrt

fun main() {
    println("Valor x1")
    var x1 = readln().toDouble()
    println("Valor x2")
    var x2 = readln().toDouble()
    println("Valor y1")
    var y1 = readln().toDouble()
    println("Valor y2")
    var y2 = readln().toDouble()
    
    var distancia = sqrt((x2 - x1).pow(2) + (y2 - y1).pow(2)) 
    
    println("Distancia é $distancia")
}

```

## Exercicio 11
```
import kotlin.math.pow

fun main(){
    var A = 0
    var B = 0
    var C = 0
    while(true){
    A = readln().toInt()
    B = readln().toInt()
    C = readln().toInt()
    if(A > 0 && B > 0 && C > 0){
        break
    } else {
        println("Todos os numeros devem ser positivos")
    }
    }
    val R = ((A + B).toDouble()).pow(2)
    val S = ((B + C).toDouble()).pow(2)
    val D = (R + S)/ 2

    
    println(D)
}

```
## Exercicio 12
```
import kotlin.math.pow

fun main(){
    var custoFabrica = readln().toFloat()
    var percentagemDistribuidor = custoFabrica * 0.28
    var imposto = custoFabrica * 0.45
    var total = custoFabrica + imposto + percentagemDistribuidor
    
    println(total)
}


```
## Exercicio 13
```
fun main(){
    var a = readln().toDouble()
    var b = readln().toDouble()
    var c = readln().toDouble()
    var d = readln().toDouble()
    var e = readln().toDouble()
    var f = readln().toDouble()
    
    var x = ((c * e) - (b * f)) / ((a * e) - (b * d))
    
    var y = ((a * f) - (c * d)) / ((a * e) - (b * d))
    
    println("O x = $x e o y = $y")
}

```

## Exercicio 14
```
fun main(){
    var salario = readln().toDouble()
    var novoSalario = salario * 1.25
    
    println(novoSalario)
}
```

## Exercicio 15
```
fun main(){
    var salario = readln().toDouble()
    var percentual = readln().toDouble()
    var novoSalario = salario * (1 + percentual / 100)
    
    println(novoSalario)
}


```
## Exercicio 16
```
fun main() {
    println("Ano de Nascimento")
    var anoNascimento = readln().toInt()
    println("Mes de Nascimento")
    var mesNascimento = readln().toInt()
    println("Dia de Nascimento")
    var diaNascimento = readln().toInt()
    println("Ano atual")
    var anoAtual = readln().toInt()
    println("Mes atual")
    var mesAtual = readln().toInt()
    println("Dia atual")
    var diaAtual = readln().toInt()

    var diferencaDia = 0
    var diferencaMes = 0
    var diferencaAno = 0

    if (anoNascimento == anoAtual) {
        diferencaAno = 0  
    } else {
        diferencaAno = anoAtual - anoNascimento
    }

    if (mesNascimento > mesAtual && anoNascimento != anoAtual) {
        diferencaMes = mesNascimento - mesAtual
        diferencaAno--
        diferencaMes = 12 - diferencaMes
    } else if (mesNascimento > mesAtual && anoNascimento == anoAtual) {
        diferencaMes = mesNascimento - mesAtual
        diferencaMes = 12 - diferencaMes 
    } else {
        diferencaMes = mesAtual - mesNascimento
    }

    if (diaNascimento > diaAtual && mesNascimento >= mesAtual) {
        diferencaDia = diaNascimento - diaAtual
        diferencaMes--
        diferencaDia = 30 - diferencaDia
    } else if (diaNascimento > diaAtual && mesNascimento < mesAtual) {
        diferencaDia = diaNascimento - diaAtual
        diferencaDia = 30 - diferencaDia
    } else {
        diferencaDia = diaAtual - diaNascimento
    }

    if (diferencaDia == 30) {
        diferencaDia = 0
    }
    println("Você tem $diferencaAno ano(s), $diferencaMes mes(es) e $diferencaDia dia(s)")
}

```

## Exercicio 17
```
fun main(){
    var sacoRacao = readln().toDouble()
    var racaoParaGato = readln().toInt()
    
    var gastoTotal = (sacoRacao * 1000) - ((racaoParaGato * 2) * 5)
    
    println("O gasto total foi $gastoTotal")
}

```

## Exercicio 18
```
fun main(){
    var A = readln().toInt()
    var B = readln().toInt()
    var temp = B
    println("Antes")
    println("Valor A = $A")
    println("Valor B = $B")
    B = A
    A = temp
    println("Depois")
    println("Valor A = $A")
    println("Valor B = $B")
}

```
## Exercicio 19
```
fun main(){
    var comprimento = readln().toInt()
    var largura = readln().toInt()
    var altura = readln().toInt()
    
    var volume = comprimento * altura * largura
    
    println(volume)
}

```
## Exercicio 20
```
fun main(){
    var comprimento = readln().toInt()
    var largura = readln().toInt()
    var altura = readln().toInt()
    
    var volume = comprimento * altura * largura
    
    println(volume)
}

```
## Exercicio 21
```
fun main() {
    var valorDolar = readln().toDouble()
    var cotacaoDolar = readln().toDouble()
    
    var valorReal = valorDolar * cotacaoDolar
    
    println(valorReal)
    
}

```

## Exercicio 22
```
import kotlin.math.pow

fun main() {
    var A = readln().toDouble()
    var B = readln().toDouble()
    var C = readln().toDouble()
    
    var quadradoResultado = (A + B + C).pow(2)
    
    println(quadradoResultado)
}

```
## Exercicio 23
```
fun main() {
    val a = 19
    val b = 49

    println("Soma: ${a + b}")
    println("Subtração: ${a - b}")
    println("Multiplicação: ${a * b}")
    println("Divisão: ${a / b}")
}
```
## Exercicio 24
```
import kotlin.math.pow

fun main() {
    var raio = readln().toDouble()
    val pi = 3.1459
    var volume = (4/3) * pi * raio.pow(3)
    
    println(volume)
}

```
## Exercicio 25
```
fun main() {
    var num = readln().toInt()
    var sucessor = num + 1
    var antecessor = num - 1

    println("Sucessor = $sucessor. Antecessor = $antecessor")
}
```
