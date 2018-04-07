# CommentProj

## List all comments
GET /comments

Example:
GET http://localhost:8080/comments
[
    {
        "id": 1,
        "text": "This is a kosher comment. Respectful and descent"
    },
    {
        "id": 2,
        "text": "This is a good comment."
    }
]

## POST a comment

POST /comments

Body: { "text" : "Your text" }

NOTE: if you want to update an existing comment provide the comment ID in the JSON Body
e.g:
    {
        "id": 1,
        "text": "This is a Update to comment Id 1"
    }

## OFFENSIVE Comment is not allowed

POST 
 {
        "text": "This is a bad comment."
  }
  
Response:

{
    "timestamp": "2018-04-07T08:20:40.913+0000",
    "status": 406,
    "error": "Not Acceptable",
    "message": "Offensive Comment!!!",
    "path": "/comments"
}
