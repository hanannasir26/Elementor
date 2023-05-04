# Elementor
Elementor Page Builder Custom Widgets

Elementor Custom Widget is created based on client requirments. Providing the reusibility concept.

The website admin just need to drag and drop the widget and complete the input fields to develop the page UI/UX.

Calling Elementor Custom Widget Directly in your theme Functions.php

  
add_action('init', function()
{ 

  if(did_action('elementor/loaded'))
  { 
      require_once DIR . '/elementor_templates/elementor_custom_widget.php'; \Elementor\Plugin::instance()->widgets_manager->register_widget_type( new ElementorPostswidget() ); 
  }

});


