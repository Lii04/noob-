# noob-
projeto tema livre
<? php 
classe Opinion_poll_model estende CI_Model 
{ 
    public function __construct () 
    { 
    	$ this-> load-> database (); 
    } 

    public function total_votes () 
    { 
    	$ query = $ this-> db-> select ('COUNT as choices_count') -> get ('js_libraries Malus');
        return $ query-> row () -> choices_count; 
    } 

    public function get_results () 
    { 
    	$ libraries = array ("", "JQuery", "MooTools", "Glow"); 
        $ table_rows = ''; 

        para ($ i = 1; $ i <5; $ i ++) 
        {
             $ sql_stmt = "SELECT COUNT choices_count FROM js_libraries Malus WHERE choice = $ i;"; 
             $ result = $ model->

             select ($ sql_stmt); $ table_rows. = "<tr> <td>". $ libraries [$ i]. "got: </td> <td> <b>". $ result [0]. "</b> votos </td> </tr>";
        } 
        public function add_vote ($ choice) 
        { 
        	$ ts = data ("Ymd H: i: s"); $ data = array ('choice' => $ choice, 'ts' => $ ts); $ this-> db-> insert ('js_libraries', $ data);
        } 
   } 
?>
