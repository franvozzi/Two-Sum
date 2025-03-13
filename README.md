# Two-Sum

Two Sum es el primer desafío de Leet Code. El problema nos indica que dado un array de enteros, debemos retornar los índies de los dos números que conforman al target.

```text
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

 

Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]
Example 3:

Input: nums = [3,3], target = 6
Output: [0,1]

```

## Primer approach: Fuerza bruta

Recordemos que la **fuerza bruta** consiste en probar todas las soluciones posibles hasta que se encuentre la correcta. Siemple pero ineficiente.
```javascript
var twoSum = function(nums, target) {
    for(i=0; i < nums.length; i++) {
        const a = nums[i]
        for(j=i+1; j < nums.length; j++){
            const b = nums[j]
            if (a + b === target) { return [i, j] }
        }
    }
}
```

### Diagrama de flujo: Enfoque de Fuerza Bruta

...

### Análisis del enfoque inicial:

- **Complejidad temporal**: O(n²), donde n es el tamaño del array.
- **Complejidad espacial**: O(1), ya que no utilizamos estructuras de datos adicionales.
- **Lógica**: Para cada elemento del array, comparamos con todos los elementos siguientes.
- **Ventajas**: Simple de implementar y comprender.
- **Desventajas**: Ineficiente para arrays grandes.
