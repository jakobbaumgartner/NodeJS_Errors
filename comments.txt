Error Handling
------------------------------

1.Technical / Network Errors
	-> tell admin database is down, tell user it is down
2."Expected" Errors
	-> for example if server is overloaded, tell user to retry
3.Bugs / Logical Errors
	-> fix during development!
	-> sometimes we get Errors thrown (.catch()), sometimes we arent that lucky

"throw new Error('fdfdf')" 
	-> build in keyboard and object
	-> vrže nam napako

za SINHRONSKO lahko kodo zapakiramo v:

try { koda ...
} catch (error) {
	error koda
}

če sedaj vrže error se bo koda izvajala tudi od napake naprej, 
dobili pa bomo error, lahko pošljemo npr. response ali pa console.log error

za ASINHRONSKO pa naredimo .than in .catch

če v then ali catch throw error in jo ujamemo v catch z next(error), 
lahko upiorabimo special middleware, ki se izvede v primeru napake
app.use(error, req, res, next) 

z .status(401) ali podobno lahko nastavimo status code






