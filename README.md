1. Написать программу, которая создает карту с именами людей и их возрастами. Добавить нового человека и вывести все записи на экран.

2. Реализовать функцию, которая принимает карту и возвращает средний возраст всех людей в карте.

3. Написать программу, которая удаляет запись из карты по заданному имени.

4. Написать программу, которая считывает строку с ввода и выводит её в верхнем регистре.

5. Написать программу, которая считывает несколько чисел, введенных пользователем, и выводит их сумму.

6. Написать программу, которая считывает массив целых чисел и выводит их в обратном порядке.

main.go
```
package main

import (
	"fmt"
	"strings"
)

func main() {
	// task_1
	fmt.Print("\n1st task\n")
	myPeople := map[string]int{

		"Anton":  18,
		"Andrey": 19,
		"Mariya": 20,
	}

	var name string
	var age int

	var nameForDel string

	var messageUpper string

	var value1, value2, value3 int

	var arr [5]int

	fmt.Print("default map: ", myPeople)

	fmt.Print("\nEnter name: ")
	fmt.Scan(&name)
	fmt.Print("Enter age: ")
	fmt.Scan(&age)

	myPeople[name] = age

	fmt.Print("Updated map: ", myPeople)
	AverageAge(myPeople)

	fmt.Print("\n\n3rd task\nEnter name for delete: ")
	fmt.Scan(&nameForDel)
	DelPeople(nameForDel, myPeople)

	fmt.Print("\n\n4th task\nEnter the text: ")
	fmt.Scan(&messageUpper)
	ToUpperCase(messageUpper)

	fmt.Print("\n\n5th task\nEnter 3 value:\n")
	fmt.Scan(&value1)
	fmt.Scan(&value2)
	fmt.Scan(&value3)

	SummValues(value1, value2, value3)

	fmt.Print("\n\n6th task\nEnter 5 numbers:\n")
	for i := 0; i < len(arr); i++ {
		fmt.Scan(&arr[i])
	}
	ReversedArray(arr)
}

// task_2
func AverageAge(MyPeoples map[string]int) {

	sum := 0

	for _, age := range MyPeoples {
		sum += age
	}
	fmt.Print("\n\n2nd task\nAverage age - ", sum/len(MyPeoples))
}

// task_3
func DelPeople(name string, MyPeoples map[string]int) {
	delete(MyPeoples, name)
	fmt.Print(MyPeoples)
}

// task_4
func ToUpperCase(text string) {

	uppCase := strings.ToUpper(text)
	fmt.Print(uppCase)

}

// task_5
func SummValues(a int, b int, c int) {

	fmt.Print("summ - ", a+b+c)

}

// task_6
func ReversedArray(arr [5]int) {
	fmt.Print("Reversed array - ")
	for i := len(arr) - 1; i >= 0; i-- {
		fmt.Print(arr[i], " ")
	}

}

```
![{A0B46980-4F92-4A42-97A1-7E9B9CE73053}](https://github.com/user-attachments/assets/1b403116-8bc5-43c1-b55c-67e715591c1e)
