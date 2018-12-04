---
UID: NF:tsgauthenticationengine.ITSGAuthenticateUserSink.DisconnectUser
title: ITSGAuthenticateUserSink::DisconnectUser
author: windows-sdk-content
description: Notifies Remote Desktop Gateway (RD Gateway) that it should disconnect the client.
old-location: termserv\itsgauthenticateusersink_disconnectuser.htm
tech.root: termserv
ms.assetid: 03385453-066d-40a9-bcbb-9623e4fdfadc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DisconnectUser, DisconnectUser method [Remote Desktop Services], DisconnectUser method [Remote Desktop Services],ITSGAuthenticateUserSink interface, ITSGAuthenticateUserSink interface [Remote Desktop Services],DisconnectUser method, ITSGAuthenticateUserSink.DisconnectUser, ITSGAuthenticateUserSink::DisconnectUser, termserv.itsgauthenticateusersink_disconnectuser, tsgauthenticationengine/ITSGAuthenticateUserSink::DisconnectUser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tsgauthenticationengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGAuthenticationEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGAuthenticationEngine.h
api_name:
 - ITSGAuthenticateUserSink.DisconnectUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSGAuthenticateUserSink::DisconnectUser


## -description


Notifies Remote Desktop Gateway (RD Gateway) that it should disconnect the client.


## -parameters




### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies the connection to disconnect. Use the value that was passed by the <a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The authentication plug-in can use this method to disconnect the client as needed. For example, it can call this method if the client's cookie expires.




## -see-also




<a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a>



<a href="https://msdn.microsoft.com/6cc0dca7-1bc7-4229-9f3b-74d600776210">ITSGAuthenticateUserSink</a>
 

 

