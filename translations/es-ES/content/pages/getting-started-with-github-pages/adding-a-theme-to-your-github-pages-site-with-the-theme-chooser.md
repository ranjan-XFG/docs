---
title: Agregar un tema a tu sitio de Páginas de GitHub con el selector de tema
intro: 'Puedes añadir un tema a tu sitio de {% data variables.product.prodname_pages %} para personalizar la apariencia de tu sitio.'
redirect_from:
  - /articles/creating-a-github-pages-site-with-the-jekyll-theme-chooser
  - /articles/adding-a-jekyll-theme-to-your-github-pages-site-with-the-jekyll-theme-chooser
  - /articles/adding-a-theme-to-your-github-pages-site-with-the-theme-chooser
  - /github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-with-the-theme-chooser
product: '{% data reusables.gated-features.pages %}'
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Pages
shortTitle: Agregar un tema al sitio de Páginas
permissions: 'People with admin permissions for a repository can use the theme chooser to add a theme to a {% data variables.product.prodname_pages %} site.'
---

## Acerca del selector de temas

{% ifversion pages-custom-workflow %}

{% note %}

**Nota**: El selector de tema de Jekyll no es compatible para los sitios de {% data variables.product.prodname_pages %} que se publican con un flujo de trabajo de {% data variables.product.prodname_actions %} personalizado. Si compilas tu sitio con Jekyll y lo publicas con un flujo de trabajo de {% data variables.product.prodname_actions %} personalizado, puedes agregar un tema editando el archivo `_config.yml`. Para obtener más información, consulta "[Agregar un tema a tu sitio de GitHub Pages con Jekyll](/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll)".

{% endnote %}

{% endif %}

El selector de temas agrega un tema de Jekyll a tu repositorio. Para obtener más información acerca de Jekyll, consulta "[Acerca de las {% data variables.product.prodname_pages %} y Jekyll](/articles/about-github-pages-and-jekyll)".

La forma en que funciona el selector de temas depende de si tu repositorio es público o privado.
  - Si las {% data variables.product.prodname_pages %} ya están habilitadas para tu repositorio, el selector de temas agregará tu tema a la fuente de publicación actual.
  - Si tu repositorio es público y {% data variables.product.prodname_pages %} se encuentra inhabilitado para éste, mediante el selector de temas podrás habilitar {% data variables.product.prodname_pages %} y configurar la rama predeterminada como tu fuente de publicación.
  - Si tu repositorio es público, y las {% data variables.product.prodname_pages %} están inhabilitadas para tu repositorio, debes habilitar las {% data variables.product.prodname_pages %} configurando una fuente de publicación antes de poder usar el selector de temas.

Para obtener más información acerca de las fuentes de publicación, consulta "[Acerca de las {% data variables.product.prodname_pages %}](/articles/about-github-pages#publishing-sources-for-github-pages-sites)".

Si antes agregaste manualmente un tema de Jekyll a tu repositorio, puede que esos archivos se apliquen incluso después de que uses el selector de temas. Para evitar conflictos, elimina todas las carpetas y archivos de temas agregados manualmente antes de usar el selector de temas. Para obtener más información, consulta "[Agregar un tema a tu sitio de {% data variables.product.prodname_pages %} con Jekyll](/articles/adding-a-theme-to-your-github-pages-site-using-jekyll)".

## Agregar un tema con el selector de temas

{% data reusables.pages.navigate-site-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.pages.sidebar-pages %}
3. Debajo de "{% data variables.product.prodname_pages %}", haz clic en **Choose a theme** (Elegir un tema) o **Change theme** (Cambiar tema). ![Elija un botón del tema](/assets/images/help/pages/choose-a-theme.png)
4. Para elegir un tema, haz clic en el tema que quieras y luego haz clic en **Select theme** (Seleccionar tema). ![Opciones de temas y botón Select theme (Seleccionar tema)](/assets/images/help/pages/select-theme.png)
5. Puede que se te solicite que edites el archivo *README.md* de tu sitio.
   - Para editar el archivo más tarde, haz clic en **Cancel** (Cancelar). ![Enlace de cancelación al editar un archivo](/assets/images/help/pages/cancel-edit.png)
   - Para editar el archivo ahora, consulta la sección "[Editar archivos](/repositories/working-with-files/managing-files/editing-files)".

El tema elegido se aplicará automáticamente a los archivos markdown de tu repositorio. Para aplicar el tema a los archivos HTML de tu repositorio, debes agregar el texto preliminar de YAML que especifica un diseño para cada archivo. Para obtener más información, consulta "[Texto preliminar](https://jekyllrb.com/docs/front-matter/)" en el sitio de Jekyll.

## Leer más

- [Temas](https://jekyllrb.com/docs/themes/) en el sitio de Jekyll
