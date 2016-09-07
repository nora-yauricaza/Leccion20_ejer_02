# Leccion20_ejer_02

Nota: Modificar el siguiente script para que muestre el resultado correcto. 
El código muestra el mensaje JS coders love its callbacks, mientras que el resultado debería ser JS developers love its closures.

var feature = 'closures'; 

(function () {    

	if ( typeof feature === 'undefined' ){     
	
		var feature = 'callbacks';    
		
		console.log('JS coders love its ' + feature );   
		
	} else { 
	
		console.log('JS developers love its ' + feature );    
		
	} 
	
})();

Cuando se ejecuta el resultado es: JS coders love its callbacks, porque tenemos dos variables con el mismo nombre (una global y otra local), 
cuando el código comienze a ejecutarse el hoisting declara la variable local sea elevada al inicio, pero solamente la declara el valor (undefined),
entonces la primera funcion se ejecuta: JS coders love its callbacks, por que el valor local tiene más peso.

var feature = 'closures'; 

(function () {    

	if ( typeof feature === 'undefined' ){     
	
		feature = 'callbacks';    
		
		console.log('JS coders love its ' + feature );   
		
	} else { 
	
		console.log('JS developers love its ' + feature );    
		
	} 
	
})();

Entonces la solución es que tenga la variable global como unica variable (HE ELIMINADO LA PRIMERA LA PALABRA (var) 

var feature = 'callbacks'; la primara condición no se cumple, entonces se ejecuta la segunda sentencia. La respuesta es: JS developers love its
