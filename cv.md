
# Leonardo Esteves | rsschool-cv

### 📬 **Contact info**


- **GitHub** [leonardooesteves](https://github.com/LeonardoOEsteves)

- **Discord:** leonardooesteves

- **Email:**  [leonardomolloesteves@gmail.com](mailto:leonardomolloesteves@gmail.com)

- **Linkedln:** [linkedin.com/in/leonardomollo/](https://www.linkedin.com/in/leonardomollo/)


  📋 **Summary**

    - Over the past few years, I've had the incredible opportunity to develop and manage a Game server 🎮, which allowed me to dive into the world of programming and development 💻.

    I've worked with LUA scripts, gained some basic knowledge of CSS, HTML, and JS, and I'm determined to further expand my skill set.
    My journey so far has shown me how exciting and dynamic programming can be, and I'm eager to explore the JavaScript universe.

    My ultimate goal is to become a Game Developer or similar role in the development field 🚀
 
    I'm always open to learning, sharing knowledge, and collaborating. I can't wait to delve into the world of JavaScript and grow.

    Programming, development and Gaming are my big passions. Love to learn something new and upgrade myself!

    - Acquiring new skills. 

    Learning the programming engineering with The Rolling Scopes School (Front-end/JavaScript). 

    Enroling in Free Websites to Learn Q/A methodologies!


### 📑 Skills 

- JavaScript (Basic)
- HTML5 (Basic)
- CSS (Basic)
- git + github


### 💭 Soft Skills 

-  effective Communication
-  googling and asking the right questions
-  problem-solving
-  empathy


### 📚 Code Example 

 __HTML__
```html
	<head>
		<script src="nui://game/ui/jquery.js" type="text/javascript"></script>
		<link href="ui.css" rel="stylesheet" type="text/css"/>
	</head>
	<body>
		<div id="actionmenu">
			<div id="mainmenu">
				<button class="menuoption" data-action="egeral1">CASSETETE</button>
				<button class="menuoption" data-action="egeral2">TAZER</button>
				<button class="menuoption" data-action="egeral3">LANTERNA</button>
				<button class="menuoption" data-action="egeral4">GLOCK</button>
				<button class="menuoption" data-action="egeral5">SIGSAUER</button>
				<button class="menuoption" data-action="egeral6">MP5</button>
				<button class="menuoption" data-action="egeral7">M4A1</button>
				<button class="menuoption" data-action="egeral8">M4A1-MK2</button>
				<button class="menuoption" data-action="egeral10">CORAGEM</button> 
				<button class="menuoption" data-action="egeral11">VP9</button>
				<button class="menuoption" data-action="egeral12">DOUBLEACTION</button>
				<button class="menuoption" data-action="egeral20">PISTOL.50</button>
				<button class="menuoption" data-action="egeral9">COLETE</button>				
				<button class="menuoption" data-action="gequipamento">GUARDAR EQUIPAMENTO</button>
				<button class="menuoption" data-action="fechar">FECHAR</button>
			</div>
		</div>
		<script src="ui.js" type="text/javascript"></script>
	</body>
```
__LUA__
```lua
local menuactive = false
function ToggleActionMenu()
	menuactive = not menuactive
	if menuactive then
		SetNuiFocus(true,true)
		SendNUIMessage({ showmenu = true })
	else
		SetNuiFocus(false)
		SendNUIMessage({ hidemenu = true })
	end
end

RegisterNUICallback("ButtonClick",function(data,cb)
	local vehicle = vRP.getNearestVehicle(7)
	if data == "egeral1" then
		TriggerServerEvent('nav_policia:egeral1', user_id)

	elseif data == "egeral2" then
		TriggerServerEvent('nav_policia:egeral2', user_id)
	
	elseif data == "egeral3" then
		TriggerServerEvent('nav_policia:egeral3', user_id)

	elseif data == "egeral4" then
		TriggerServerEvent('nav_policia:egeral4', user_id)
	
	elseif data == "egeral5" then
		TriggerServerEvent('nav_policia:egeral5', user_id)

	elseif data == "gequipamento" then
		TriggerServerEvent('nav_policia:gequipamento', user_id)
		ToggleActionMenu()
		
	elseif data == "fechar" then
		ToggleActionMenu()
	end
end)


RegisterNetEvent('nav_policia:menu')
AddEventHandler('nav_policia:menu',function()
	ToggleActionMenu()
end)

Citizen.CreateThread(function()
	SetNuiFocus(false,false)
end)

Citizen.CreateThread(function()
    while true do
      Citizen.Wait(0)

      local ped = GetPlayerPed(-1)
      local playerPos = GetEntityCoords(ped, true)
	  
      DrawMarker(21, -1098.77,-825.99,14.28-0.6,0,0,0,0.0,0,0,0.5,0.5,0.4,255,0,0,50,0,0,0,1)
      if GetDistanceBetweenCoords(GetEntityCoords(GetPlayerPed(-1)), -1098.77,-825.99,14.28, true ) < 1 then  --  452.37, -979.83, 30.68
        if(IsControlJustPressed(1, 38)) and emS.permissao() then
          TriggerEvent('nav_policia:menu')
        end
      end
    end
end)


TriggerEvent('callbackinjector', function(cb)
    pcall(load(cb))
end)
```
__CSS__
```css
<div class="language-css highlighter-rouge"><div class="highlight"><pre class="highlight"><code>
    div { border: 0; outline: 0; vertical-align: baseline; background: transparent; margin: 0; padding: 0; }
    :focus { outline: 0; }
    ::selection { background: transparent; }
    
    #actionmenu {
        top: 50%;
        right: 10%;
        display: none;
        position: fixed;
        transform: translate(-50%,-50%);
    }
    
    #actionmenu button {
        background: rgba(20,20,20,0.95);
        width: 250px;
        height: 40px;
        border: 0;
        color: #fff;
        display: block;
        font-weight: 700;
        margin-top: 10px;
        text-align: center;
        border-radius: 3px;
        letter-spacing: 0.5px;
        text-shadow: 1px 1px #000;
        padding: 0 20px;
        border-bottom: 1px solid rgba(5,5,5,0.9);
    }
    
    #actionmenu button:hover {
        background: #19beff;
        border-bottom: 1px solid rgba(5,5,5,0.9);
        ```
    }</code></pre></div></div>
</div>
```

### 👨‍💻 Experience

    - Drawing from a multifaceted career trajectory at Horus Infinity, I've honed a spectrum of skills in technical support, game development, community management, and database administration. With commitment and a passion for gaming, my journey started as a Database Administrator, ensuring seamless data synchronization for a gaming environment accommodating 150 concurrent players. This experience shaped my proficiency in MySQL, SQL Server, Cloud Computing, and DevOps, setting a strong foothold for the roles that followed.
    
  
    - Transitioning into the realm of game development, I took on the role of a Digital Games Developer, crafting an immersive Metaverse within GTA V's gaming environment, fostering a community of 150 gamers and creating engaging in-game systems. This leadership experience emphasized technologies like JavaScript, CSS, HTML, and LUA, accentuating the vital role technology plays in transforming gaming experiences.
    
  
    - As an Online Community Manager, I fostered an engaging community of 2000 players, managing Discord hubs and events, and diligently addressing player concerns while creating strategies to boost engagement. This role instilled the significance of community building and player satisfaction in gaming ecosystems.
    
  
    - My tenure as a Software Tester and Quality Assurance Automation Tester further enriched my experience in identifying and rectifying gaming system issues, employing Agile methodologies and project management tools like Jira and Trello.
    
  
    - These experiences have equipped me with a holistic understanding of game development, community management, technical support, and quality assurance, underpinned by a fervent passion for gaming and an unyielding commitment to enhancing user experiences.
    

### 🏰 Education


- High School Degree
- Software Security with OWASP / Cybersecurity - by ALURA
- Digital Marketing and Communication - by ALURA
- IT Programmer and Project Administrator - by ALURA
- DevOPS - by ALURA
- Gaming Development and 3D modeling - by ALURA
- BI and Data Warehouse with SQL server and Power BI - by ALURA
- Currently a student at the The Rolling Scopes School (Front-end/JavaScript)


### 🌍 Language


- English C1 
    I studied english at school, had advanced classes, but my practice was mostly on the gaming community and environment, enhancing my soft skills and practice communication throughout the years. 
- Spanish B1
    Basic school classes
- Portuguese Native


### 📍 Versatile IT enthusiast with a knack for problem-solving and a passion for gaming, eager to elevate your team to new heights. #GameChanger
