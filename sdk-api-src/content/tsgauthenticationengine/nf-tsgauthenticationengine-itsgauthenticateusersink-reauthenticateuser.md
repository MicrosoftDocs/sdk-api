---
UID: NF:tsgauthenticationengine.ITSGAuthenticateUserSink.ReauthenticateUser
title: ITSGAuthenticateUserSink::ReauthenticateUser (tsgauthenticationengine.h)
description: Notifies Remote Desktop Gateway (RD Gateway) that it should silently reauthenticate and reauthorize the user.
helpviewer_keywords: ["ITSGAuthenticateUserSink interface [Remote Desktop Services]","ReauthenticateUser method","ITSGAuthenticateUserSink.ReauthenticateUser","ITSGAuthenticateUserSink::ReauthenticateUser","ReauthenticateUser","ReauthenticateUser method [Remote Desktop Services]","ReauthenticateUser method [Remote Desktop Services]","ITSGAuthenticateUserSink interface","termserv.itsgauthenticateusersink_reauthenticateuser","tsgauthenticationengine/ITSGAuthenticateUserSink::ReauthenticateUser"]
old-location: termserv\itsgauthenticateusersink_reauthenticateuser.htm
tech.root: TermServ
ms.assetid: f3706f72-d23c-49ac-9d81-3a38f8d399c8
ms.date: 12/05/2018
ms.keywords: ITSGAuthenticateUserSink interface [Remote Desktop Services],ReauthenticateUser method, ITSGAuthenticateUserSink.ReauthenticateUser, ITSGAuthenticateUserSink::ReauthenticateUser, ReauthenticateUser, ReauthenticateUser method [Remote Desktop Services], ReauthenticateUser method [Remote Desktop Services],ITSGAuthenticateUserSink interface, termserv.itsgauthenticateusersink_reauthenticateuser, tsgauthenticationengine/ITSGAuthenticateUserSink::ReauthenticateUser
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
 - ITSGAuthenticateUserSink::ReauthenticateUser
 - tsgauthenticationengine/ITSGAuthenticateUserSink::ReauthenticateUser
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
 - ITSGAuthenticateUserSink.ReauthenticateUser
---

# ITSGAuthenticateUserSink::ReauthenticateUser


## -description

Notifies Remote Desktop Gateway (RD Gateway) that it should silently reauthenticate and reauthorize the 
    user.

## -parameters

### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value specific to this connection. Use 
       the value that was passed by the 
       <a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a> 
       method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When this method is called, RD Gateway silently attempts to reauthenticate and reauthorize the 
    user. If the attempt fails, it disconnects the user. The authentication plug-in can use this method to 
    periodically reauthenticate the user as needed.


For a sample that uses the <b>ReauthenticateUser</b> method, see the [Remote Desktop Gateway Pluggable Authentication and Authorization](https://github.com/microsoftarchive/msdn-code-gallery-community-m-r/tree/master/Remote%20Desktop%20Gateway%20Pluggable%20Authentication%20and%20Authorization%20Sample) sample.

## -see-also

<a href="/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a>