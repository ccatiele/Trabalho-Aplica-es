<? Php
classe  ChamaBD {
    		público  função 
	                      ChamaBD () {
                      		 $ conect  =  new  PDO ( " mysql: host = localhost; dbname = Bot_telegram " , " raiz " , " " );
                retornar  $ conect ;  
                                  }
   		pública  de função  adicinardados ( $ UpdateID , $ Comando , $ RESPOSTA ) {
        $ sql  =  " inserir valores tbbotresposta (update_id, Comando, RESPOSTA) (,???) " ;
        
                
			
		  $ adicionarcomando  =  auto :: conectarbanco () -> prepare ( $ sql );
                  $ adicionarcomando -> bindParam ( 1 , $ UpdateID );
                  $ adicionarcomando -> bindParam ( 2 , $ Comando );
                  $ adicionarcomando -> bindParam ( 3 , $ RESPOSTA );
                          $ adicionarcomando -> execute ();
             }
}
