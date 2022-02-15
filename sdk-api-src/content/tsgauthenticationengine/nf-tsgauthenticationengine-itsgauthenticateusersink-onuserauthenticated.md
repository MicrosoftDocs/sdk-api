---
UID: NF:tsgauthenticationengine.ITSGAuthenticateUserSink.OnUserAuthenticated
title: ITSGAuthenticateUserSink::OnUserAuthenticated (tsgauthenticationengine.h)
description: Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in has successfully authenticated the user.
helpviewer_keywords: ["ITSGAuthenticateUserSink interface [Remote Desktop Services]","OnUserAuthenticated method","ITSGAuthenticateUserSink.OnUserAuthenticated","ITSGAuthenticateUserSink::OnUserAuthenticated","OnUserAuthenticated","OnUserAuthenticated method [Remote Desktop Services]","OnUserAuthenticated method [Remote Desktop Services]","ITSGAuthenticateUserSink interface","termserv.itsgauthenticateusersink_onuserauthenticated","tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticated"]
old-location: termserv\itsgauthenticateusersink_onuserauthenticated.htm
tech.root: TermServ
ms.assetid: 2f3dd498-661c-4787-8db4-bcc43bd76294
ms.date: 12/05/2018
ms.keywords: ITSGAuthenticateUserSink interface [Remote Desktop Services],OnUserAuthenticated method, ITSGAuthenticateUserSink.OnUserAuthenticated, ITSGAuthenticateUserSink::OnUserAuthenticated, OnUserAuthenticated, OnUserAuthenticated method [Remote Desktop Services], OnUserAuthenticated method [Remote Desktop Services],ITSGAuthenticateUserSink interface, termserv.itsgauthenticateusersink_onuserauthenticated, tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticated
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSGAuthenticateUserSink::OnUserAuthenticated
 - tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - TSGAuthenticationEngine.h
api_name:
 - ITSGAuthenticateUserSink.OnUserAuthenticated
---

# ITSGAuthenticateUserSink::OnUserAuthenticated


## -description

Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in has successfully authenticated the user.

## -parameters

### -param userName [in]

The name of the user who initiated the connection.

### -param userDomain [in]

The domain of the user who initiated the connection.

### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies this connection. Use the value that was passed by the <a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a> method.

### -param userToken [in, optional]

A pointer to a <b>HANDLE</b> that specifies the user token of the user. If the user is not running Windows, set this parameter to <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can call this method from your implementation of <a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a>. If authentication requires more than 1 second, we recommend launching a separate thread to perform authentication.

For a sample that uses the <b>OnUserAuthenticated</b> method, see the [Remote Desktop Gateway Pluggable Authentication and Authorization](https://github.com/microsoftarchive/msdn-code-gallery-community-m-r/tree/master/Remote%20Desktop%20Gateway%20Pluggable%20Authentication%20and%20Authorization%20Sample) sample.

## -see-also

<a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a>



<a href="/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a>