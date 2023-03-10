---
UID: NF:tsgauthenticationengine.ITSGAuthenticateUserSink.DisconnectUser
title: ITSGAuthenticateUserSink::DisconnectUser (tsgauthenticationengine.h)
description: Notifies Remote Desktop Gateway (RD Gateway) that it should disconnect the client.
helpviewer_keywords: ["DisconnectUser","DisconnectUser method [Remote Desktop Services]","DisconnectUser method [Remote Desktop Services]","ITSGAuthenticateUserSink interface","ITSGAuthenticateUserSink interface [Remote Desktop Services]","DisconnectUser method","ITSGAuthenticateUserSink.DisconnectUser","ITSGAuthenticateUserSink::DisconnectUser","termserv.itsgauthenticateusersink_disconnectuser","tsgauthenticationengine/ITSGAuthenticateUserSink::DisconnectUser"]
old-location: termserv\itsgauthenticateusersink_disconnectuser.htm
tech.root: TermServ
ms.assetid: 03385453-066d-40a9-bcbb-9623e4fdfadc
ms.date: 12/05/2018
ms.keywords: DisconnectUser, DisconnectUser method [Remote Desktop Services], DisconnectUser method [Remote Desktop Services],ITSGAuthenticateUserSink interface, ITSGAuthenticateUserSink interface [Remote Desktop Services],DisconnectUser method, ITSGAuthenticateUserSink.DisconnectUser, ITSGAuthenticateUserSink::DisconnectUser, termserv.itsgauthenticateusersink_disconnectuser, tsgauthenticationengine/ITSGAuthenticateUserSink::DisconnectUser
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
 - ITSGAuthenticateUserSink::DisconnectUser
 - tsgauthenticationengine/ITSGAuthenticateUserSink::DisconnectUser
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
 - ITSGAuthenticateUserSink.DisconnectUser
---

# ITSGAuthenticateUserSink::DisconnectUser


## -description

Notifies Remote Desktop Gateway (RD Gateway) that it should disconnect the client.

## -parameters

### -param context [in]

A pointer to  a <b>ULONG</b> that contains  a value that identifies the connection to disconnect. Use the value that was passed by the <a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The authentication plug-in can use this method to disconnect the client as needed. For example, it can call this method if the client's cookie expires.

## -see-also

<a href="/windows/desktop/api/tsgauthenticationengine/nf-tsgauthenticationengine-itsgauthenticationengine-authenticateuser">AuthenticateUser</a>



<a href="/windows/desktop/api/tsgauthenticationengine/nn-tsgauthenticationengine-itsgauthenticateusersink">ITSGAuthenticateUserSink</a>