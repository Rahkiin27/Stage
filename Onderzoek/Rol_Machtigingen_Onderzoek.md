# Hoofdvraag: Hoe kan ik toegangscontrole voor gebruikers implementeren?
>   Het doel is om een gebruiker bepaalde machtigingen te geven om dingen te doen in de applicatie. Zo mag een gebruiker met een machtiging tot bijvoorbeeld magazijnadministratie de voorraad van het magazijn zien en beheren. Een gebruiker die niet deze machtiging heeft mag het bijvoorbeeld alleen bekijken en niet beheren.

# Deelvraag 1: Wat is de beste manier om iemand machtigingen te geven?
>   Hiervoor heb ik eerst zelf een implementatie bedacht en mijn idee uitgewerkt in pseudo-UML. [Hier](./Rol_Machtigingen_Idee.png) is een PNG van dit diagram. Na wat meer onderzoek te doen via google blijkt dit voor deze use case ook de beste optie te zijn. Deze vorm van Role Based Authorization heet [Role Based Access Control](https://nl.wikipedia.org/wiki/Role-based_access_control).

# Deelvraag 2: Hoe kan ik een filter voor een functionaliteit zetten?
>   Voor deze vraag heb ik een klein bibliotheekonderzoek gedaan, ik heb op google gezocht met de query: "c# mvc role authorization". Hierdoor kwam ik op een [example](https://www.c-sharpcorner.com/UploadFile/rahul4_saxena/role-based-access-of-an-mvc-application/) uit waarin stond dat je ook zelf een AuthorizeAttribute kan maken door van deze klasse te erven. Na dit gelezen te hebben heb ik een klein labonderzoek uitgevoerd om te testen of dit daadwerkelijk kon waaruit bleek dat dit ook echt kan.

# Deelvraag 4: Hoe kan ik overerving toepassen op bepaalde, maar niet alle rollen?
>   Het doel is om hierarchische relaties tussen bepaalde rollen te kunnen maken zodat het mogelijk is om wanneer je een machtiging uit een bepaalde rol haalt, bij de children van deze rol de machtigingen ook worden weggehaald. Als je op google zoekt naar "sql child parent relationships" is vrijwel het eerste wat je tegen komt het gebruik van een parentId. Dit is de simpelste en ook een goede oplossing voor deze use case. Aangezien je alleen, als er überhaupt een child is, het Id van de parent aan parentId hoeft te linken.
