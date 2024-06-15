# Setting-up-Active-Directory-on-our-Windows-Server-2019
<h1>Summary</h1>

<img width="350" alt="Screenshot 2024-06-15 at 12 26 48 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/623fa216-e56d-43b7-b6ae-5efd468d5f16">

In this lab we are going to log into our Windows 2019 VM and create a local administrator. From there we will go through the steps to install Active Directory.

<h1>What is Active Directory?</h1>

Active Directory allows us to create rules within a network. We can create users and authenticate them via a password. We can create group policy objects and apply them to different users. We also can also group users into organizational units so we may easily assign rules to multiple users



<h1>Step 1) Creating a Local Admin Account</h1>

<h2>Summary</h2>

In this step we will create a local administrator account. This account will not be associated with our setup of active directory but it will allow us to get into the computer if something goes wrong with our server.

<h2>1A) Booting up our Windows 2019 Server VM for the first time</h2>

Double click on the Server VM we have created

<img width="278" alt="Screenshot 2024-05-19 at 1 24 07 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/edf6a435-0ef3-4560-b278-051a1c207d96">

That should open our window where we can use our VM as shown below

<img width="504" alt="Screenshot 2024-05-19 at 1 25 31 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/c57aff0c-7311-490f-82ea-7117966ad7dc">

Once at this screen you can fill out the options that best suit you

<img width="505" alt="Screenshot 2024-05-19 at 1 27 03 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/77544fb8-975e-4606-8235-8990998ce72e">

Once configured click next

<img width="506" alt="Screenshot 2024-05-19 at 1 28 23 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/258f6cf3-146d-44c2-8946-1d1ffd69658b">

Then click Install now
You will then be prompted with this screen

<img width="509" alt="Screenshot 2024-05-19 at 1 29 23 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/5bee363c-e0c1-4bd6-a510-83ad2649fc9a">

Make sure you select one of the two desktop experience options or else you will just have access to command line

Once you have selected one of the Desktop experiences you can click next

Accept the Licensing Agreement

<img width="509" alt="Screenshot 2024-05-19 at 1 35 30 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/5b344a7e-d76a-4a76-8eeb-70ba6c6c96bd">

Click Next

Click Custom: Install Windows only (advanced)

<img width="507" alt="Screenshot 2024-05-19 at 1 37 15 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/e33d06ff-c0a1-4365-b2dc-674e1cc44f66">

Now you can see the 50 GB we alloted in the setup of our VM

<img width="509" alt="Screenshot 2024-05-19 at 1 42 54 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/183faedb-8611-41f5-a155-7ae37304a968">

We don't want to change anything so you can click next

Now the VM will install our Windows Server 2019! It may take awhile so hang tight.

<img width="507" alt="Screenshot 2024-05-19 at 1 44 51 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/cf67f34e-d74d-4a07-bf58-2995b9e1c756">
<h2>1B) Creating the Local Admin Account </h2>

Once its finished you will see this screen. We will create an administrator account so we can set up Active Directory 

<img width="509" alt="Screenshot 2024-05-19 at 2 01 07 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/b55026f6-e9f0-4a06-b591-4ef43211f0ca">

Once you have created a password you can click finish

Now we are going to sign in with the administrator account that we just created

<img width="506" alt="Screenshot 2024-05-19 at 2 04 45 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/45e56e3e-c296-47a3-836f-57598b34823c">

Once you have successfully logged in you will see this screen

<h1>Step 2) Installing Active Directory</h1>

<h2>Summary</h2>

Now that we have created a local administrator account and logged in we can now create our Active Directory Domain.


<img width="509" alt="Screenshot 2024-05-19 at 2 07 07 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/154dcdea-9e8a-4e44-b8f9-5a3fe4579425">

To install Active Directory we will navigate to the top right and click on manage followed by add roles and features

<img width="512" alt="Screenshot 2024-05-19 at 2 08 04 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/89ed63ec-a64c-49d9-9994-ad1d72a06716">

After selecting add roles and features you will see this screen

<img width="509" alt="Screenshot 2024-05-19 at 2 09 19 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/e371555a-8b6e-4a07-b7a9-671087bb7035">

Click next on the bottom of the window

<img width="510" alt="Screenshot 2024-05-19 at 2 12 53 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/0989bc75-c42c-49fc-8c8e-426a364a4508">

Since Active Directory is a role based feature we will click next

<img width="512" alt="Screenshot 2024-05-19 at 2 15 29 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/43ff8ecd-c1c2-4344-9bd4-604b00835b8e">

When prompted with the screen above you will see we have an option selected. Within that option we have 3 fields. The name is the name of the computer (which we are currently using). The IP address of this computer is also shown (you may want to keep that written down somewhere for when we want to connect computers to our domain). Finally we see the Operating system this computer is running on.

These options are what we want so you can click the next button

<img width="508" alt="Screenshot 2024-05-19 at 2 21 10 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/8a1a6699-c0d0-41b3-8e4e-e949017cb90d">

We are going to select the Active Directory Domain Services checkmark.

<img width="510" alt="Screenshot 2024-05-19 at 2 23 20 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/770f7a84-0a60-43eb-87f4-7e4783553ac7">

Once you see this screen you will click the add features button

<img width="505" alt="Screenshot 2024-05-19 at 2 24 16 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/ae49ebfb-0a89-49e5-b995-258401eeb7cf">

Once you see the screen above you may click next

<img width="503" alt="Screenshot 2024-05-19 at 2 25 10 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/7ca67886-4202-456d-9885-0a75e11a7777">

Click next again 

<img width="508" alt="Screenshot 2024-05-19 at 2 25 45 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/d703b8db-8022-41ef-813c-7e930e8e7cba">

Click next one more time

<img width="508" alt="Screenshot 2024-05-19 at 2 26 44 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/b4a0d999-f434-4175-8d2d-5b83b8b1cb1d">

Finally you will click Install (This may take a couple minutes)

<img width="507" alt="Screenshot 2024-05-19 at 2 27 30 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/c9380f17-25a2-4e97-b087-da9616a217df">

<img width="510" alt="Screenshot 2024-05-19 at 2 29 23 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/fbffd194-469f-41d2-b388-357c83f76973">

Once completed you will see this message you may click close

<img width="505" alt="Screenshot 2024-05-19 at 2 30 30 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/5f321968-962f-4b9b-bd2a-46efbd2fcf08">

Click on the flag pole with the warning sign

<img width="504" alt="Screenshot 2024-05-19 at 2 33 25 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/ba61c258-0a5a-4b0c-b290-dffef771b843">

Click on promote this server to domain controller

Now we get to set up our Domain! Since we do not have a forest we will create one

<img width="509" alt="Screenshot 2024-05-19 at 2 35 36 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/adba5cac-dd5f-4db5-a26a-e1fdac401e4e">

You can name your domain whatever you'd like just make sure it ends in .org, .net, etc

<img width="368" alt="Screenshot 2024-05-19 at 2 39 37 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/50ee71cf-76fc-4c02-90ff-040dac9437ca">

We will then click next

<img width="505" alt="Screenshot 2024-05-19 at 2 41 33 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/fdfdb24d-59c3-49c6-a1dc-6767f9202292">

You may then create your DSRM password and click next

<img width="507" alt="Screenshot 2024-05-19 at 2 43 48 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/7b7ac109-d3cc-4590-9051-e15150e27141">

We don't need to change DNS options so click next

<img width="509" alt="Screenshot 2024-05-19 at 2 45 01 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/e5e56131-473f-4c3b-b9c4-3ab2b7ab6c34">

Click next again

<img width="509" alt="Screenshot 2024-05-19 at 2 45 48 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/17a80831-a393-4f0a-8f11-dfbe5cfdffad">

Click next again

<img width="509" alt="Screenshot 2024-05-19 at 2 46 37 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/b150f061-37fa-4030-8a66-88317d60204a">

click next again

<img width="506" alt="Screenshot 2024-05-19 at 2 47 30 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/dc11740f-c9ff-4271-9c8d-3af70c18463c">

Finally click install. This may take awhile

<img width="497" alt="Screenshot 2024-05-19 at 2 52 29 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/39a03752-4f8c-4f0f-8853-1ba733426b6d">

Once completed your computer will restart. This will also take a bit of time.

<img width="505" alt="Screenshot 2024-05-19 at 3 41 57 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/0f65b2e3-b74a-47ca-8377-d4febea1563f">

Now we will sign in with our admin account we created for our domain 

<img width="507" alt="Screenshot 2024-05-19 at 3 43 06 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/309e1c91-b794-4a93-98f0-77bbe1299937">

After signing in our server Manager will load

<img width="510" alt="Screenshot 2024-05-19 at 3 44 42 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/0e2e70e3-56b7-4edb-a400-fdd658714c07">

Click tools in the top right

<img width="508" alt="Screenshot 2024-05-19 at 3 45 26 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/21ac6787-e316-4669-a346-c5206a3238c0">

Then select Active Directory Users and Computers

<img width="509" alt="Screenshot 2024-05-19 at 3 47 15 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/7f1d8f76-10cb-4db3-a7a5-ef3908dca997">

Now we can see the Domain we created!

<img width="507" alt="Screenshot 2024-05-19 at 3 48 01 PM" src="https://github.com/Jtalbert15/Setting-up-Active-Directory-on-our-Windows-Server-2019/assets/66844406/c6a819c7-6d5f-41df-97b5-e970073639f2">

Congratulations! That concludes the setup for Active Directory! 
