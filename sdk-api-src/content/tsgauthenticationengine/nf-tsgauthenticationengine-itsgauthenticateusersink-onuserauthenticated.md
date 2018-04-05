---
UID: NF:tsgauthenticationengine.ITSGAuthenticateUserSink.OnUserAuthenticated
title: ITSGAuthenticateUserSink::OnUserAuthenticated method
author: windows-driver-content
description: Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in has successfully authenticated the user.
old-location: termserv\itsgauthenticateusersink_onuserauthenticated.htm
old-project: TermServ
ms.assetid: 2f3dd498-661c-4787-8db4-bcc43bd76294
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: ITSGAuthenticateUserSink, ITSGAuthenticateUserSink interface [Remote Desktop Services], OnUserAuthenticated method, ITSGAuthenticateUserSink::OnUserAuthenticated, OnUserAuthenticated method [Remote Desktop Services], OnUserAuthenticated method [Remote Desktop Services], ITSGAuthenticateUserSink interface, OnUserAuthenticated,ITSGAuthenticateUserSink.OnUserAuthenticated, termserv.itsgauthenticateusersink_onuserauthenticated, tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticated
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
req.typenames: TC_IFC_DESCRIPTOR, *PTC_IFC_DESCRIPTOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	TSGAuthenticationEngine.h
api_name:
-	ITSGAuthenticateUserSink.OnUserAuthenticated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITSGAuthenticateUserSink::OnUserAuthenticated method


## -description


Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in has successfully authenticated the user.


## -parameters




### -param userName [in]

The name of the user who initiated the connection.


### -param userDomain [in]

The domain of the user who initiated the connection.


### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies this connection. Use the value that was passed by the <a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a> method.


### -param userToken [in, optional]

A pointer to a <b>HANDLE</b> that specifies the user token of the user. If the user is not running Windows, set this parameter to <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can call this method from your implementation of <a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a>. If authentication requires more than 1 second, we recommend launching a separate thread to perform authentication.


#### Examples

For an example that uses the 
     <b>OnUserAuthenticated</b> method, see 
     <a href="https://Code.MSDN.Microsoft.Com/Remote-Desktop-Gateway-517d6273">Remote Desktop Gateway Pluggable Authentication and Authorization Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a>



<a href="https://msdn.microsoft.com/6cc0dca7-1bc7-4229-9f3b-74d600776210">ITSGAuthenticateUserSink</a>
 

 

