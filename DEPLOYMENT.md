# Guía de Deployment - GitHub Pages

## Pasos para publicar tu portafolio:

### 1. Crear repositorio en GitHub
```bash
# En GitHub, crea un nuevo repositorio llamado: username.github.io
# (reemplaza 'username' con tu nombre de usuario de GitHub)
```

### 2. Inicializar Git en output/html
```bash
cd output/html
git init
git add .
git commit -m "Initial commit: Portfolio"
```

### 3. Conectar con GitHub
```bash
git remote add origin https://github.com/username/username.github.io.git
git branch -M main
git push -u origin main
```

### 4. Habilitar GitHub Pages
1. Ve a Settings > Pages en tu repositorio
2. Selecciona la rama 'main' como source
3. Guarda los cambios

### 5. Acceder a tu portafolio
Tu portafolio estará disponible en:
`https://username.github.io`

## Actualizar el portafolio

Para actualizar tu portafolio después de hacer cambios:

```bash
# Desde el directorio raíz del proyecto
python3 scripts/deploy_to_github_pages.py

# Luego en output/html:
cd output/html
git add .
git commit -m "Update portfolio"
git push
```

## Configurar dominio personalizado (Opcional)

1. Compra un dominio
2. Crea un archivo `CNAME` en output/html con tu dominio:
   ```
   tudominio.com
   ```
3. Configura los DNS de tu dominio:
   - Tipo A: 185.199.108.153
   - Tipo A: 185.199.109.153
   - Tipo A: 185.199.110.153
   - Tipo A: 185.199.111.153

## Configurar formulario de contacto

1. Ve a [Formspree.io](https://formspree.io)
2. Crea una cuenta gratuita
3. Crea un nuevo formulario
4. Copia el endpoint URL
5. En `index.html`, reemplaza `YOUR_FORM_ID` con tu ID de Formspree

## Troubleshooting

### El sitio no se muestra
- Espera 5-10 minutos después del primer push
- Verifica que GitHub Pages esté habilitado
- Revisa que el repositorio sea público

### Imágenes no se cargan
- Verifica que las imágenes estén en `assets/images/`
- Asegúrate de que los paths sean relativos

### Formulario no funciona
- Configura Formspree como se indica arriba
- Verifica que el email en Formspree sea correcto

---

¿Necesitas ayuda? Consulta la [documentación de GitHub Pages](https://docs.github.com/pages)
