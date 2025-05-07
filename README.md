# lovethework_api_sim.py
from flask import Flask, jsonify

app = Flask(__name__) 

@app.route("/lovethework", methods=["GET"])
def get_ltw():
    return jsonify({
        "results": [
            {
                "title": "The Missing Chapter – Stayfree",
                "summary": "Una poderosa campaña de educación menstrual en India que ganó un Glass Lion.",
                "url": "https://www.lovethework.com/work-awards/2022/63006/stayfree-the-missing-chapter"
            },
            {
                "title": "Backup Ukraine – Polycam x UNESCO",
                "summary": "Un proyecto para preservar digitalmente el patrimonio ucraniano en plena guerra.",
                "url": "https://www.lovethework.com/work-awards/2022/61012/backup-ukraine"
            },
            {
                "title": "The Cost of Beauty – Dove",
                "summary": "Un retrato crudo del impacto de las redes sociales en la autoestima adolescente.",
                "url": "https://www.lovethework.com/work-awards/2023/71004/dove-the-cost-of-beauty"
            }
        ]
    })

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=3000)
