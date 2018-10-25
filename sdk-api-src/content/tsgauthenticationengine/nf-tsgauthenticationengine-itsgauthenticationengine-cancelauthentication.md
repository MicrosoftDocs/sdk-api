---
UID: NF:tsgauthenticationengine.ITSGAuthenticationEngine.CancelAuthentication
title: ITSGAuthenticationEngine::CancelAuthentication
author: windows-sdk-content
description: Cancels an existing authentication request.
old-location: termserv\itsgauthenticationengine_cancelauthentication.htm
tech.root: termserv
ms.assetid: 07da9ffa-b137-4e99-a1d1-14b7c14438a3
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CancelAuthentication, CancelAuthentication method [Remote Desktop Services], CancelAuthentication method [Remote Desktop Services],ITSGAuthenticationEngine interface, ITSGAuthenticationEngine interface [Remote Desktop Services],CancelAuthentication method, ITSGAuthenticationEngine.CancelAuthentication, ITSGAuthenticationEngine::CancelAuthentication, termserv.itsgauthenticationengine_cancelauthentication, tsgauthenticationengine/ITSGAuthenticationEngine::CancelAuthentication
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
 - ITSGAuthenticationEngine.CancelAuthentication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSGAuthenticationEngine::CancelAuthentication


## -description


Cancels an existing authentication request.

Remote Desktop Gateway (RD Gateway) calls this method when the user who initiated the connection terminates the connection, or when the connection fails.


## -parameters




### -param mainSessionId [in]

An identifier assigned to the connection request.


### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies this connection. This value should be passed back to RD Gateway by using the methods of the  <a href="https://msdn.microsoft.com/6cc0dca7-1bc7-4229-9f3b-74d600776210">ITSGAuthenticateUserSink</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c72f3f22-a403-45b0-9ccb-6339ae001024">ITSGAuthenticationEngine</a>
 

 

