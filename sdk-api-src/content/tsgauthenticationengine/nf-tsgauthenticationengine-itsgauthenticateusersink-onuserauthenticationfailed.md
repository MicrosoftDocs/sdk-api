---
UID: NF:tsgauthenticationengine.ITSGAuthenticateUserSink.OnUserAuthenticationFailed
title: ITSGAuthenticateUserSink::OnUserAuthenticationFailed (tsgauthenticationengine.h)
description: Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in failed to authenticate the user.
helpviewer_keywords: ["ITSGAuthenticateUserSink interface [Remote Desktop Services]","OnUserAuthenticationFailed method","ITSGAuthenticateUserSink.OnUserAuthenticationFailed","ITSGAuthenticateUserSink::OnUserAuthenticationFailed","OnUserAuthenticationFailed","OnUserAuthenticationFailed method [Remote Desktop Services]","OnUserAuthenticationFailed method [Remote Desktop Services]","ITSGAuthenticateUserSink interface","termserv.itsgauthenticateusersink_onuserauthenticationfailed","tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticationFailed"]
old-location: termserv\itsgauthenticateusersink_onuserauthenticationfailed.htm
tech.root: TermServ
ms.assetid: d3d1e582-db1d-413d-8ec8-7fdb7c6e3609
ms.date: 12/05/2018
ms.keywords: ITSGAuthenticateUserSink interface [Remote Desktop Services],OnUserAuthenticationFailed method, ITSGAuthenticateUserSink.OnUserAuthenticationFailed, ITSGAuthenticateUserSink::OnUserAuthenticationFailed, OnUserAuthenticationFailed, OnUserAuthenticationFailed method [Remote Desktop Services], OnUserAuthenticationFailed method [Remote Desktop Services],ITSGAuthenticateUserSink interface, termserv.itsgauthenticateusersink_onuserauthenticationfailed, tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticationFailed
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
 - ITSGAuthenticateUserSink::OnUserAuthenticationFailed
 - tsgauthenticationengine/ITSGAuthenticateUserSink::OnUserAuthenticationFailed
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
 - ITSGAuthenticateUserSink.OnUserAuthenticationFailed
---

# ITSGAuthenticateUserSink::OnUserAuthenticationFailed


## -description

Notifies Remote Desktop Gateway (RD Gateway) that the authentication plug-in failed to authenticate the user.

## -parameters

### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies this connection. Use the value that was passed by the <a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a> method.

### -param genericErrorCode [in]

A Windows error code that specifies the cause of the authentication failure.

### -param specificErrorCode [in]

This parameter is reserved. Always set this parameter to zero.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can call this method from your implementation of 
    <a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a>. If 
    authentication requires more than 1 second, we recommend launching a separate thread to perform 
    authentication.

For a sample that uses the <b>OnUserAuthenticationFailed</b> method, see the [Remote Desktop Gateway Pluggable Authentication and Authorization](https://github.com/microsoftarchive/msdn-code-gallery-community-m-r/tree/master/Remote%20Desktop%20Gateway%20Pluggable%20Authentication%20and%20Authorization%20Sample) sample.

## -see-also

<a href="/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a>