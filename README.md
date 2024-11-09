<!DOCTYPE html>
<html lang="ha">
<head>
    <meta charset="UTF-8">
    <title>Nishad - Raba Hotuna da Rubutu</title>
    <meta name="description" content="Nishad yana ba masu amfani damar raba hotuna da rubutu. Ziyarci shafin mu don samun sabbin abubuwa.">
    <meta name="keywords" content="Nishad, hotuna, rubutu, raba, shafin yanar gizo">
    <meta name="robots" content="index, follow">
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"/>
    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">

    <style>
        body {
            font-family: Arial, sans-serif;
        }

        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1em 0;
        }

        main {
            padding: 20px;
        }

        #postForm {
            margin-bottom: 20px;
        }

        #postsContainer {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .post {
            border: 1px solid #ccc;
            padding: 10px;
            background-color: #f9f9f9;
        }

        .likeButton, .editButton, .deleteButton, .commentButton {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 5px 10px; 
            cursor: pointer;
            margin-top: 10px;
            margin-right: 5px;
        }

        .likeButton:hover, .editButton:hover, .deleteButton:hover, .commentButton:hover {
            background-color: magenta;
        }

        .likeCount, .commentList {
            margin-top: 5px;
            font-weight: bold;
        }

        .commentInput {
            display: none;
            margin-top: 10px;
        }

        .comments {
            margin-top: 10px;
        }
   .fileInput {
     display: none;
   }
    .fileInput {
     display: none;
   }
   
    /* Gumaka*/
    
 body {
            
            justify-content: center; /* Tsara gumakan a tsakiya */
            align-items: center; /* Tsara gumakan a tsakiya a tsaye */
            height: 100vh; /* Tsawon jikin shafin */
            background: #f0f0f0; /* Launin bango */
            margin: 0; /* Cire margin */
        }

        .icon-container {
            display: flex; /* Amfani da flexbox don jera gumakan a layi guda */
            gap: 20px; /* Sarari tsakanin gumakan */
        }

        .icon-container a {
            text-decoration: none; /* Cire layin gado daga gumakan */
            
            font-size: 40px; /* Girman gumakan */
        }

        .icon-container a:hover {
            color: #007bff; /* Launin gumakan lokacin da aka hover */
        }
     /* i */
     
     button {
      background-image: linear-gradient(#dafa, rebeccapurple, dodgerblue, #badada); 
     }
     i[class="fab fa-whatsapp"]
     ,[class="fa fa-phone"] {
       width: 300;
       height: 150;
       color: #4CAF50;
     
       
     background-image: linear-gradient(
  
 cyan, 
 rebeccapurple,
 blue,  magenta
);
 } 
    
     i[class="fa fa-comment"]
     ,[class="fa fa-envelope"] {
       color: #333;
        width: 300;
        height: 150;
        background-image: linear-gradient(
  
       cyan, 
       rebeccapurple,
       blue,  magenta
       );
       }
    
    .icon-container {
    display: flex;
    gap: 15px; /* Domin tsari mai kyau */
}

.icon-container a {
    text-decoration: none;
    color: #333; /* Launin gumakan */
    transition: transform 0.3s ease; /* Motsin yana canza tsawon lokaci */
}

.icon-container a:hover {
    transform: scale(1.2); /* Wadannan gumakan suna girma idan aka zabe su */
    text-shadow: 0 0 10px rgba(0, 0, 0, 0.3); /* Don ƙarin haske idan ana zaban */
}

/* Optional: Motsi a hankali a lokacin da shafin ya loda */
.icon-container a {
    animation: float 2s infinite ease-in-out; /* Motsi na madauki */
}

@keyframes float {
    0% {
        transform: translateY(0px);
    }
    50% {
        transform: translateY(-20px); /* Motsi sama */
    }
    100% {
        transform: translateY(0px);
    }
}
/* A */
  
 a { background-image: linear-gradient(
  
 cyan, 
 rebeccapurple,
 blue,  magenta
);
 }  

 
</style>



</head> 
<body>
    
  <div class="ad">
    <h2>Tallace-tallace na Kai</h2>
    <a href="https://example.com" target="_blank">
        <img src="Hotuna/Muhammadu.jpg" alt="Tallace-tallace" style="width: 100%; max-width: 300px;">
    </a>
</div>

    
    <header>
        <h1>Shafin Raba Hotuna da Rubutu</h1>
    </header>

<h2>Maraba da Nishad!</h2>
 <p>Wannan shafin yana ba ku damar raba hotuna da rubutu tare da sauran masu amfani.</p>


<main>
<form id="postForm">
<button type="button" class="chooseFileButton" onclick="document.getElementById('postImage').click()" style="font-size: 19px;"> <i style="font-size: 40px;" class="material-icons">camera</i><h1> Ɗauki Hoton</h1></button>
<input type="file" id="postImage" name="camera" accept="image/*" capture="camera" class="fileInput">
<button type="button" class="chooseFileButton" onclick="document.getElementById('postImage').click()" style="font-size: 19px;"> <i style="font-size: 40px;" class="material-icons">attachment</i><h1> Zaɓi Hoton</h1></button>
<input type="file" id="postImage" accept="image/*"  class="fileInput">
<textarea id="postContent" placeholder="Rubuta abin da kake so..." required></textarea><button type="submit"><i style="font-size: 40px;;" class="material-icons">send</i></button>
</form>
 <div id="postsContainer"></div>
 </main>
       
    <script>
        document.getElementById('postForm').addEventListener('submit', function(event) {
            event.preventDefault();

            const postContent = document.getElementById('postContent').value;
            const postImage = document.getElementById('postImage').files[0];
            const postDiv = document.createElement('div');
            postDiv.classList.add('post');

            const imageElement = document.createElement('img');
            if (postImage) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    imageElement.src = e.target.result;
                    imageElement.style.maxWidth = "100%";
                    postDiv.appendChild(imageElement);
                };
                reader.readAsDataURL(postImage);
            }

            const contentElement = document.createElement('p');
            contentElement.textContent = postContent;
            postDiv.appendChild(contentElement);

            // Like button and count
            const likeButton = document.createElement('button');
            likeButton.innerHTML = '<i style="font-size:50px;" class="fa fa-thumbs-up"></i>'; // Gunki na "Like" tare da rubutu

            likeButton.classList.add('likeButton');
            const likeCount = document.createElement('div');
            likeCount.classList.add('likeCount');
            likeCount.textContent = 'Likes: 0';

            let likes = 0; // Initialize likes count
            likeButton.onclick = function() {
                likes = (likes === 0) ? 1 : 0; // Toggle likes
                likeCount.textContent = 'Likes: ' + likes; // Update likes count
            };

            postDiv.appendChild(likeButton);
            postDiv.appendChild(likeCount);

            // Comment section
            const commentButton = document.createElement('button');
            commentButton.innerHTML = '<i style="color: white;" class="fa fa-comment">Comment</i>';
            commentButton.classList.add('commentButton');
            postDiv.appendChild(commentButton);

            const commentInput = document.createElement('input');
            commentInput.type = 'text';
            commentInput.placeholder = 'Rubuta sharhi...';
            commentInput.classList.add('commentInput');
            postDiv.appendChild(commentInput);

            const commentList = document.createElement('div');
            commentList.classList.add('comments');
            postDiv.appendChild(commentList);

            commentButton.onclick = function() {
                commentInput.style.display = (commentInput.style.display === 'none' || commentInput.style.display === '') ? 'block' : 'none';
            };

            commentInput.addEventListener('keypress', function(event) {
                if (event.key === 'Enter' && commentInput.value !== '') {
                    const commentElement = document.createElement('div');
                    commentElement.textContent = commentInput.value;
                    commentList.appendChild(commentElement);
                    commentInput.value = '';
                }
            });

            // Edit button
            const editButton = document.createElement('button');
            editButton.textContent = '🛠️️ Gyara';
            editButton.classList.add('editButton');
            postDiv.appendChild(editButton);
            
            editButton.onclick = function() {
                contentElement.contentEditable = true;
                contentElement.focus();
                contentElement.addEventListener('blur', function() {
                    contentElement.contentEditable = false;
                });
            };

            // Delete button
            const deleteButton = document.createElement('button');
            deleteButton.innerHTML = '<i class="fa fa-trash">Share</i>';
            deleteButton.classList.add('deleteButton');
            postDiv.appendChild(deleteButton);
            
            deleteButton.onclick = function() {
                postDiv.remove();
            };

            document.getElementById('postsContainer').prepend(postDiv);
            document.getElementById('postForm').reset();
        });
    </script>

<h1>Domin Ƙarinn bayani</h1>
<div class="icon-container">
    <a href="mailto:yuktamyuktam1@gmail.com" aria-label="Email yuktamyuktam1@gmail.com"<i class="fa fa-envelope"></i> Email</a>
    <a href="tel:+218920517942" aria-label="Call phone +218920517942"><i class="fa fa-phone"></i> Call phone</a>
    <a href="smsto:+218920517942?body=message_text" aria-label="Send SMS to +218920517942"> <i class="fa fa-comment"></i> Message text </a>
    <a href="whatsapp://send?text=message_text&phone=+218920517942" aria-label="Send WhatsApp message to +218920517942"><i class="fab fa-whatsapp"></i> WhatsApp</a>

</body>
</html>
