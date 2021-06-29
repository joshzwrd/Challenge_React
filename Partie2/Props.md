# Props 

**Qu'est-ce qu'un Props ?**

- **Props** est un objet invisible qui est générer automatiquement afin de récupérer des données

**Exemple :**

Dans le bout de code suivant voici on a ajouté des propriétés a notre élément **`<Eleve>`**

Dans mon **groupe d’entraid**e il y a une fille qui s’appelle **Eva Dupont** et qui a **15** de moyenne.

    class App extends Component {
    render() {
        return (
            <div classeName="App">
                <h1>Groupe d'entraide</h1>
                <Eleve nom="Eva Dupont" Moyenne="15"/>
            </div>
        );
    }
    }

Grâce React les données de **`<Eleve>`** sont directement stocker dans un **props** afin de pouvoir les reutiliser


    class Eleve extends Component {
        render(){
            return (
            <div className="eleve">
                <h1>{this.props.nom}</h1>
                <p>Moyenne scolaire : {this.props.moyenne}/20</p>
            </div>
            
            );
        }
    }

Ici les données invisible de props son reutiliser directement à l'interieur de la class **`<Eleve>`**

Pour faire appêl au données de props, il faut utiliser les accolades **{this.props.données}**

this veut désigné l'objet en cours !

**{this.props.nom} :** tu vas me recupérer là propriété nom de l'objet en cours

# Composant Fonctionnel

Dans un composant fonctionnel on utilise une fonction fléchées

**En 3 Méthodes** 

N°1 :

    const Eleve = props => {
            return (
                <div className="eleve">
                <h1>{props.nom}</h1>
                <p>Moyenne scolaire : {props.moyenne}/20</p>
            </div>
            );
        }

N°2 :

    const Eleve = props =>
                    <div className="eleve">
                    <h1>{props.nom}</h1>
                    <p>Moyenne scolaire : {props.moyenne}/20</p>
                </div>
                ;

N°3 :

    const Eleve = props => <div className="eleve">
                    <h1>{props.nom}</h1>
                    <p>Moyenne scolaire : {props.moyenne}/20</p>
                </div>;


Dans ce cas là on a pas besoin d'utiliser le **this**

Ces 3 méthodes fonctionne également et renvoie le même résultat que notre class initial néanmoins on perd en lisibilité plus on simplifie notre code.

