using System;
using System.Windows.Forms;
using System.Drawing;

namespace GYM_Los_Ayala
{
    public partial class FormPrincipal : Form
    {
        public FormPrincipal()
        {
            InitializeComponent();
        }

        private void InitializeComponent()
        {
            this.Text = "GYM Los Ayala - Sistema de Gestión";
            this.ClientSize = new Size(800, 500);
            this.StartPosition = FormStartPosition.CenterScreen;

            // Título principal
            Label lblTitulo = new Label()
            {
                Text = "BIENVENIDO AL GYM LOS AYALA",
                Location = new Point(150, 30),
                Font = new Font("Arial", 16, FontStyle.Bold),
                Size = new Size(500, 40)
            };

            Label lblSubtitulo = new Label()
            {
                Text = "Sistema de Gestión Integral",
                Location = new Point(250, 75),
                Font = new Font("Arial", 12),
                Size = new Size(300, 20)
            };

            // Botones del menú principal
            Button btnGestionAparatos = new Button()
            {
                Text = "📋 Gestión de Aparatos",
                Location = new Point(200, 130),
                Size = new Size(400, 50),
                Font = new Font("Arial", 12, FontStyle.Bold)
            };
            btnGestionAparatos.Click += (s, e) => AbrirFormulario(new FormGestionAparatos(), "Gestión de Aparatos");

            Button btnUsuarios = new Button()
            {
                Text = "👥 Usuarios",
                Location = new Point(200, 200),
                Size = new Size(400, 50),
                Font = new Font("Arial", 12, FontStyle.Bold)
            };
            btnUsuarios.Click += (s, e) => AbrirFormulario(new FormUsuarios(), "Gestión de Usuarios");

            Button btnProductos = new Button()
            {
                Text = "📦 Productos",
                Location = new Point(200, 270),
                Size = new Size(400, 50),
                Font = new Font("Arial", 12, FontStyle.Bold)
            };
            btnProductos.Click += (s, e) => AbrirFormulario(new FormProductos(), "Gestión de Productos");

            Button btnPagos = new Button()
            {
                Text = "💰 Pagos",
                Location = new Point(200, 340),
                Size = new Size(400, 50),
                Font = new Font("Arial", 12, FontStyle.Bold)
            };
            btnPagos.Click += (s, e) => AbrirFormulario(new FormPagos(), "Gestión de Pagos");

            Button btnExpedientes = new Button()
            {
                Text = "📄 Expedientes",
                Location = new Point(200, 410),
                Size = new Size(400, 50),
                Font = new Font("Arial", 12, FontStyle.Bold)
            };
            btnExpedientes.Click += (s, e) => AbrirFormulario(new FormExpedientes(), "Gestión de Expedientes");

            this.Controls.AddRange(new Control[] {
                lblTitulo, lblSubtitulo,
                btnGestionAparatos, btnUsuarios, btnProductos, btnPagos, btnExpedientes
            });
        }

        private void AbrirFormulario(Form formulario, string titulo)
        {
            formulario.Show();
        }
    }
}
