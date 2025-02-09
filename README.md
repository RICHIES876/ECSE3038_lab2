the purpose for writting this code was for an assignment. The objective of the assignmnet is to expose me to "get" and "post" request handler. 
    On that note, the creation of "get" function, this allowed for the user to return the content from a list. Where the path/route to the content which is "/person"
    
    @app.get("/person")
async def get_people():
    return data
    Additionlly, the creation of the second "get" function is a function used to return images of my favourite pokemon and a reson for why it is my favourite pokemon. 

@app.get("/pokemon")
async def fav_pokey_image_for_extra_grade():
    html_content = """
    <html style="background-color:black">
        <head>
            <title>RICHIE Pokemon Page</title>
        </head>
        <body>
            <div style="text-align: center; width: 100%; margin: auto;border: 3px solid BLACK;">
                <h1 style="color:white">The Legendary MEWTWO</h1>
            </div>
            <div style="margin:auto; width: 100%; border: 3px solid BLACK;">
                <img width="465" height="500" style="padding-left:20px; padding-right:10px" src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/d5e34c18-c95a-4d77-8b31-5972d1ad8c22/dd1ujbt-c111fc75-5680-40ee-a25f-8cfe563551b4.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7InBhdGgiOiJcL2ZcL2Q1ZTM0YzE4LWM5NWEtNGQ3Ny04YjMxLTU5NzJkMWFkOGMyMlwvZGQxdWpidC1jMTExZmM3NS01NjgwLTQwZWUtYTI1Zi04Y2ZlNTYzNTUxYjQucG5nIn1dXSwiYXVkIjpbInVybjpzZXJ2aWNlOmZpbGUuZG93bmxvYWQiXX0.j4FcpgNedfKfhmOYh3OMsOAthCjcyxgxyb2wMPLN3s8"/>
                <img width="465" height="500"style="padding-left: 10px; padding-right:20px" src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/ac1b678d-1ec0-45e8-b1ba-24b37e5eec3b/d65s6xy-2bbf10f5-e339-41fc-ac2c-e2d1b43e046d.jpg/v1/fill/w_903,h_884,q_70,strp/mewtwo_by_kicktyan_d65s6xy-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9OTc5IiwicGF0aCI6IlwvZlwvYWMxYjY3OGQtMWVjMC00NWU4LWIxYmEtMjRiMzdlNWVlYzNiXC9kNjVzNnh5LTJiYmYxMGY1LWUzMzktNDFmYy1hYzJjLWUyZDFiNDNlMDQ2ZC5qcGciLCJ3aWR0aCI6Ijw9MTAwMCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.aC4YFSJDcH4rdjjwjTQSWMg90-1NQrDig2rxoYq0w1k"/>
                <img width="465" height="500" style="padding-left:2px" src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/35715733-8786-4d50-9c56-6790474b278c/de2awz2-c60c4f10-e25c-4f13-a581-514e9e1372ed.jpg/v1/fill/w_1920,h_1358,q_75,strp/mew_and_mewtwo_by_dekunobou_kizakura_de2awz2-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTM1OCIsInBhdGgiOiJcL2ZcLzM1NzE1NzMzLTg3ODYtNGQ1MC05YzU2LTY3OTA0NzRiMjc4Y1wvZGUyYXd6Mi1jNjBjNGYxMC1lMjVjLTRmMTMtYTU4MS01MTRlOWUxMzcyZWQuanBnIiwid2lkdGgiOiI8PTE5MjAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.kYgybQnoG2r2zCMQk_57uiuDSutU1NUHYeyzGVz7gPw"/>
            </div>
            <h2 style="color:white"> REASON: </h2> 
            <h3 style="color:white">  Personally, if had the opportunity to gain supernatural abilities Mewtwo would be my direct go to, just just having all that raw power and thought of being unstoppable and alway in control is just me thats one of my main reason <h3>
    """
    return HTMLResponse(content=html_content, status_code=200)

     The final the creation "post" function was implemented to sent a request to the server to update it with the required content of the user name, address, and occupation, if not satisfied it server with respond with a invalid condition. 

     @app.post("/person")
async def create_item(person:Item):

    if person.name  and person.address and person.occupation:
        data.append(person) 
        return jsonable_encoder(person)
    else:
        return "invalid request"