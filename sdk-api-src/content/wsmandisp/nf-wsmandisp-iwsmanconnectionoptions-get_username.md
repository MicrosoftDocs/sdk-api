---
UID: NF:wsmandisp.IWSManConnectionOptions.get_UserName
title: IWSManConnectionOptions::get_UserName
author: windows-sdk-content
description: Sets and gets the user name of a local or a domain account on the remote computer. This property determines the user name for authentication.
old-location: winrm\iwsmanconnectionoptions_username.htm
tech.root: WinRM
ms.assetid: 7b20fcac-0481-4619-aa57-f72318a9a68d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWSManConnectionOptions interface [Windows Remote Management],UserName property, IWSManConnectionOptions.UserName, IWSManConnectionOptions.get_UserName, IWSManConnectionOptions::UserName, IWSManConnectionOptions::get_UserName, IWSManConnectionOptions::put_UserName, UserName property [Windows Remote Management], UserName property [Windows Remote Management],IWSManConnectionOptions interface, get_UserName, winrm.iwsmanconnectionoptions_username, wsmandisp/IWSManConnectionOptions::UserName, wsmandisp/IWSManConnectionOptions::get_UserName, wsmandisp/IWSManConnectionOptions::put_UserName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManConnectionOptions.UserName
 - IWSManConnectionOptions.get_UserName
 - IWSManConnectionOptions.put_UserName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsmandisp.h
: 
- IWSManConnectionOptions.get_UserName
: 
---

# IWSManConnectionOptions::get_UserName


## -description


Sets and gets the user name of a local or a domain account on the remote computer. This property determines the user name for authentication. If no value is supplied and the <b>WSManFlagCredUsernamePassword</b> flag is not set, then the user name of the account that is running the script is used.

 If the <b>WSManFlagCredUsernamePassword</b> flag is set but no user name is specified, the script prompts the user to enter the user name and password. If no user name and password are entered then an access denied error is returned. For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>.

This property is read/write.


## -parameters


## -remarks



You can supply <a href="https://msdn.microsoft.com/e8f70143-f002-4b39-97a3-006b9713262d">UserName</a> and <a href="https://msdn.microsoft.com/61ba54b6-7da0-423e-b5b2-c4dd8aacd042">Password</a> for a domain account when using <a href="windows_remote_management_glossary.htm">Negotiate</a> or <i>Kerberos</i> authentication, or for a local account with <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">Basic</a> authentication.  To connect to a local account, the <a href="https://msdn.microsoft.com/299d9a95-bd30-414c-996d-6633e8b7ce52">WSMan.CreateSession</a> flags must contain the combination of the <b>WSManFlagUseBasic</b>flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. To connect to a domain account, the <b>WSMan.CreateSession</b> flags must contain the combination of the <b>WSManFlagUseNegotiate</b>flag and  the <b>WsmanFlagCredUserNamePassword</b> flag, or the combination of the <b>WSManFlagUseKerberos</b>flag and  the <b>WsmanFlagCredUserNamePassword</b> flag. For a domain account, <b>UserName</b> must be specified in the form "computer\username", where the "computer" part of the string can be either the name or the IP address. For more information, see <a href="https://msdn.microsoft.com/97a13b07-ae7a-4d2f-8841-77a22c91b204">Authentication for Remote Connections</a>.




## -see-also




<a href="https://msdn.microsoft.com/e8f70143-f002-4b39-97a3-006b9713262d">ConnectionOptions.UserName</a>



<a href="https://msdn.microsoft.com/940097da-c5bb-4170-a2aa-fcbbee622fe6">IWSManConnectionOptions</a>
 

 

