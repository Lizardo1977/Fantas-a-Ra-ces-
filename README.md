<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Referidos por fuente</title>
    https://cdn.jsdelivr.net/npm/chart.jsscript>
</head>
<body>

    <div style="width: 700px; margin: 50px auto;">
        <canvas id="referidosChart"></canvas>
    </div>

    <script>
        const ctx = document.getElementById('referidosChart');

        new Chart(ctx, {
            type: 'bar',
            data: {
                labels: ['Facebook', 'Enlace directo o QR', 'Instagram'],
                datasets: [{
                    label: 'Cantidad de referidos',
                    data: [6, 2, 1],
                    backgroundColor: [
                        '#1877F2',
                        '#34A853',
                        '#E1306C'
                    ],
                    borderColor: '#000',
                    borderWidth: 1
                }]
            },
            options: {
                responsive: true,
                plugins: {
                    title: {
                        display: true,
                        text: 'Referidos por fuente'
                    }
                },
                scales: {
                    y: {
                        beginAtZero: true,
                        ticks: {
                            stepSize: 1
                        }
                    }
                }
            }
        });
    </script>

</body>
</html>
