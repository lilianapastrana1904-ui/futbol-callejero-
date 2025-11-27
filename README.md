from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def inicio():
    return render_template('index.html')

@app.route('/Torneo')
def torneo():
    return render_template('torneo.html')  # o cultura.html si lo tienes

@app.route('/Cultura')
def cultura():
    return render_template('cultura.html')  # si aún no existe, puedes crear ese HTML

@app.route('/Cambiemos el cuento')
def cuentos():
    return render_template('cuentos.html')

@app.route('/Musicoterapia')
def musicoterapia():
    return render_template('musica.html')

@app.route('/Cursos de ingles')
def cursos():
    return render_template('cursos.html')

@app.route('/Beneficiarios')
def beneficiarios():
    return render_template('beneficios.html')

@app.route('/Salud')
def salud():
    return render_template('salud.html')

@app.route('/Contacto')
def contacto():
    return render_template('contacto.html')

if __name__ == '__main__':
    app.run(debug=True)
