---
UID: NF:tsgauthenticationengine.ITSGAuthenticationEngine.AuthenticateUser
title: ITSGAuthenticationEngine::AuthenticateUser (tsgauthenticationengine.h)
description: Authenticates a user.helpviewer_keywords: ["AuthenticateUser","AuthenticateUser method [Remote Desktop Services]","AuthenticateUser method [Remote Desktop Services]","ITSGAuthenticationEngine interface","ITSGAuthenticationEngine interface [Remote Desktop Services]","AuthenticateUser method","ITSGAuthenticationEngine.AuthenticateUser","ITSGAuthenticationEngine::AuthenticateUser","termserv.itsgauthenticationengine_authenticateuser","tsgauthenticationengine/ITSGAuthenticationEngine::AuthenticateUser"]
old-location: termserv\itsgauthenticationengine_authenticateuser.htm
tech.root: TermServ
ms.assetid: a378c28f-ecd1-43db-b998-487176f656f5
ms.date: 12/05/2018
ms.keywords: AuthenticateUser, AuthenticateUser method [Remote Desktop Services], AuthenticateUser method [Remote Desktop Services],ITSGAuthenticationEngine interface, ITSGAuthenticationEngine interface [Remote Desktop Services],AuthenticateUser method, ITSGAuthenticationEngine.AuthenticateUser, ITSGAuthenticationEngine::AuthenticateUser, termserv.itsgauthenticationengine_authenticateuser, tsgauthenticationengine/ITSGAuthenticationEngine::AuthenticateUser
f1_keywords:
- tsgauthenticationengine/ITSGAuthenticationEngine.AuthenticateUser
dev_langs:
- c++
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
- ITSGAuthenticationEngine.AuthenticateUser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSGAuthenticationEngine::AuthenticateUser


## -description


Authenticates a user.

Remote Desktop Gateway (RD Gateway) calls this method when it receives a new connection request. The authentication plug-in 
    should authenticate the user based on the cookie  referenced by the <i>cookieData</i> 
    parameter. The authentication plug-in should then use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a> interface to notify 
    RD Gateway about the result of authentication.


## -parameters




### -param mainSessionId [in]

A unique identifier assigned to the connection request by RD Gateway.


### -param cookieData [in]

A pointer to a <b>BYTE</b> that contains the cookie provided by the user.


### -param numCookieBytes [in]

The number of bytes referenced by the <i>cookieData</i> parameter.


### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value specific to this connection. This 
      value should be passed back to RD Gateway by using the methods of the 
      <a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a> interface.


### -param pSink [in]

A pointer to a 
      <a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a> interface that 
      the authentication plug-in must use to notify RD Gateway about the result of authentication.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method returns <b>S_OK</b>, RD Gateway waits for the authentication 
    plug-in to call a method of the 
    <a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a> interface. If any 
    other value is returned, RD Gateway immediately denies the  connection request.


#### Examples

For an example that uses the 
     <b>AuthenticateUser</b> method, 
     see 
     <a href="https://Code.MSDN.Microsoft.Com/Remote-Desktop-Gateway-517d6273">Remote Desktop Gateway Pluggable Authentication and Authorization Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticationengine">ITSGAuthenticationEngine</a>
 

 

