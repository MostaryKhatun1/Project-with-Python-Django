creste product:POST "/api/v1/products"
               author:Basic/Bearer token
                 body:{
                       "name":" "
                       "price":" "

                       }
             response:200 Ok=>created
                      400 =>Bad Request
                      401 =>Unathenticated
                      500 =>Server Error
    
    
GET all products:GET "/api/v1/products/{id}"
                  Author:Basic/Bearer to token
                  Body:None
                  response:
                  Body=>{jeson obj}{"id:s"}
                  code=>200 ok
                        400 unauthenticated
                        500 server error
                        404 Not found

Update product:PUT "/api/v1/products/{id}"
               Author:Basic/Beares token
               Body:PUT=>Fullobj,PATCH=>partial obj
               Response:
               Body:=>Updated obj json 
               code:200 ok
                    401 Unauthenticated
                    500 server error
                    404 Not Found
                    400 Bad Request
                                 
DELETE products:DELETE "/api/v1/product/{id}"
                Author:Basic/Bearer token
                Body:None
                Response:
                Body:=>Delete json obj/empty
                code:=>200 ok
                       401 unathenticated
                       500 server error
                       404 Not Found
                        
         
