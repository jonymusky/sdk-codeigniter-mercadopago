# MercadoPago SDK module for CodeIgniter

Usage:

1. Copy the application folder in your codeigniter application folder.

2. Modify the application/config/mercadopago.php values with the MercadoPago credentials.

Get your CLIENT_ID and CLIENT_SECRET in the following address:

    Argentina: https://www.mercadopago.com/mla/herramientas/aplicaciones
    Brazil: https://www.mercadopago.com/mlb/ferramentas/aplicacoes
    Mexico: https://www.mercadopago.com/mlm/herramientas/aplicaciones
    Venezuela: https://www.mercadopago.com/mlv/herramientas/aplicaciones


In your constructor of your controller just add:

        $CI = &get_instance();
        $CI->config->load("mercadopago", TRUE);
        $config = $CI->config->item('mercadopago');
        $this->load->library('Mercadopago', $config);   

And thats it.

You can access to the SDK methods like 


    $accessToken = $this->mercadopago->get_access_token();


