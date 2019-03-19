---
UID: NF:tsgauthenticationengine.ITSGAuthenticateUserSink.OnUserAuthenticationFailed
title: ITSGAuthenticateUserSink::OnUserAuthenticationFailed (tsgauthenticationengine.h)
author: windows-sdk-content
description: Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in failed to authenticate the user.
old-location: termserv\itsgauthenticateusersink_onuserauthenticationfailed.htm
tech.root: TermServ
ms.assetid: d3d1e582-db1d-413d-8ec8-7fdb7c6e3609
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITSGAuthenticateUserSink interface [Remote Desktop Services],OnUserAuthenticationFailed method, ITSGAuthenticateUserSink.OnUserAuthenticationFailed, ITSGAuthenticateUserSink::OnUserAuthenticationFailed, OnUserAuthenticationFailed, OnUserAuthenticationFailed method [Remote Desktop Services], OnUserAuthenticationFailed method [Remote Desktop Services],ITSGAuthenticateUserSink interface, termserv.itsgauthenticateusersink_onuserauthenticationfailed, tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticationFailed
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
 - ITSGAuthenticateUserSink.OnUserAuthenticationFailed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSGAuthenticateUserSink::OnUserAuthenticationFailed


## -description


Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in failed to authenticate the user.


## -parameters




### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies this connection. Use the value that was passed by the <a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a> method.


### -param genericErrorCode [in]

A Windows error code that specifies the cause of the authentication failure.


### -param specificErrorCode [in]

This parameter is reserved. Always set this parameter to zero.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You can call this method from your implementation of 
    <a href="https://msdn.microsoft.com/a378c28f-ecd1-43db-b998-487176f656f5">AuthenticateUser</a>. If 
    authentication requires more than 1 second, we recommend launching a separate thread to perform 
    authentication.


#### Examples

For an example that uses the 
     <b>OnUserAuthenticationFailed</b> method, see 
     <a href="https://Code.MSDN.Microsoft.Com/Remote-Desktop-Gateway-517d6273">Remote Desktop Gateway Pluggable Authentication and Authorization Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/6cc0dca7-1bc7-4229-9f3b-74d600776210">ITSGAuthenticateUserSink</a>
 

 

