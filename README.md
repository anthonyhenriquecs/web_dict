# web_dict

#Gereção de uma pagina web a partir de um dicionario
filmes = {
    "ficção": ["Circulo de fogo", "Piratas do caribe"],
    "comedia": ["american Pie", "Se beber nao case", "vizinhos"],
    "herois": ["Dr. Estranho", "Dead Poll"]
}
with open("filmes.html", "w", encoding="utf-8") as pagina:
    pagina.write("""
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<title>Filmes</title>
</head>
<body>
""")
for c, v in filmes.items():
    pagina.write(f"<h1>{c}</h1>\n")
    for e in v:
        pagina.write(f"<h2>{e}</h2>\n")
pagina.write("<boddy></html>")
