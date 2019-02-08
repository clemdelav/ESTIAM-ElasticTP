# ESTIAM-ElasticTP

Questions de Clément Delavaud

Pour que les questions 5,6,7,8 et 9 ne retournent pas d'erreur, il faut changer le type de certains champs. :
  "coord" = type : geo_point
  "borough" = fielddata : true
  "cuisine" = fielddata : true
  
  
  
  index = //localhost:9200/restaurants/_mappings/_doc ; methode = put
{
	"properties" : {
		"borough" : {         /       "cuisine"
			"type" : "text",
			"fielddata" : true
		}
	}
}



  index = //localhost:9200/restaurants/_mappings/_doc ; methode = put
{
	"properties" : {
		"address.coord" : {
			"type" : "geo_point",
		}
	}
}
