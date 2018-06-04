---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWSManConnectionOptions::put_UserName


## -description


Sets and gets the user name of a local or a domain account on the remote computer. This property determines the user name for authentication. If no value is supplied and the <b>WSManFlagCredUsernamePassword</b> flag is not set, then the user name of the account that is running the script is used.

 If the <b>WSManFlagCredUsernamePassword</b> flag is set but no user name is specified, the script prompts the user to enter the user name and password. If no user name and password are entered then an access denied error is returned. For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>.

This property is read/write.


## -parameters


## -remarks



You can supply <a href="https://msdn.microsoft.com/library/windows/hardware/dn997357">UserName</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn915695">Password</a> for a domain account when using <a href="windows_remote_management_glossary.htm">Negotiate</a> or <i>Kerberos</i> authentication, or for a local account with <a href="windows_remote_management_glossary.htm">Basic</a> authentication.  To connect to a local account, the <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a> flags must contain the combination of the <b>WSManFlagUseBasic</b>
flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. To connect to a domain account, the <b>WSMan.CreateSession</b> flags must contain the combination of the <b>WSManFlagUseNegotiate</b>
flag and  the <b>WsmanFlagCredUserNamePassword</b> flag, or the combination of the <b>WSManFlagUseKerberos</b>
flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. For a domain account, <b>UserName</b> must be specified in the form "computer\username", where the "computer" part of the string can be either the name or the IP address. For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>.




## -see-also




<a href="https://msdn.microsoft.com/e8f70143-f002-4b39-97a3-006b9713262d">ConnectionOptions.UserName</a>



<a href="https://msdn.microsoft.com/940097da-c5bb-4170-a2aa-fcbbee622fe6">IWSManConnectionOptions</a>
 

 

