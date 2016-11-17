pagamastarde-oscommerce
================

Módulo de pago de Paga+Tarde para osCommerce (v.2.2.x - 2.3.x)

## Instrucciones de Instalación

1. Crea tu cuenta en pagamastarde.com si aún no la tienes [desde aquí](https://bo.pagamastarde.com/)
2. Descarga el módulo de [aquí](https://github.com/pagantis/pagamastarde-oscommerce/releases)
3. Sube el contenido de la carpeta que coincida con tu versión de oscommerce al directorio root ( / ) de tu instalación oscommerce.
4. Si tu tienda tiene más idiomas, copia el fichero de idiomas en la carpeta correspondiente y edítalo para ajustar los textos
  - includes/languages/OTRO_IDIOMA/modules/payment/pagamastarde.php
5. Desde el panel de osCommerce de tu tienda, accede a Modulos > Pago. Pulsa el botón Instalar Módulo y selecciona el módulo Paga+Tarde.
6. Una vez instalado, selecciona el módulo Paga+Tarde de la lista de módulos disponibles y pulsa Editar.
7. Configura el código de cuenta y la clave de firma con la información de tu cuenta que encontrarás en [el panel de gestión de Paga+Tarde](https://bo.pagamastarde.com/shop). Ten en cuenta que para hacer cobros reales deberás activar tu cuenta de Paga+Tarde.

## Instucciones adicionales para osCommerce 2.2

8. Edita el fichero '/catalog/checkout_success.php' y añade justo después de la línea:
```php
require('includes/application_top.php');
```
   el siguiente código:
```php
$_SESSION['cart']->reset(true);
unset($_SESSION['cart']);
```

9. Si quieres que aparezca el simulador de cuotas a la página de checkout, debes incluir jQuery.


### Soporte

Si tienes alguna duda o pregunta no tienes más que escribirnos un email a soporte@pagamastarde.com.


### Release notes

#### 1.0.0

- Versión inicial
