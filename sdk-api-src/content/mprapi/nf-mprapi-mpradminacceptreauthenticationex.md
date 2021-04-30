---
UID: NF:mprapi.MprAdminAcceptReauthenticationEx
title: MprAdminAcceptReauthenticationEx function (mprapi.h)
description: Remote Access Service (RAS) calls the MprAdminAcceptReauthenticationEx function whenever the quarantine state of the client changes.
helpviewer_keywords: ["MprAdminAcceptReauthenticationEx","MprAdminAcceptReauthenticationEx callback","MprAdminAcceptReauthenticationEx callback function [RAS]","mprapi/MprAdminAcceptReauthenticationEx","rras.mpradminacceptreauthenticationex"]
old-location: rras\mpradminacceptreauthenticationex.htm
tech.root: RRAS
ms.assetid: 32ea0cb5-f67d-4dcc-b5d0-705b6847b163
ms.date: 12/05/2018
ms.keywords: MprAdminAcceptReauthenticationEx, MprAdminAcceptReauthenticationEx callback, MprAdminAcceptReauthenticationEx callback function [RAS], mprapi/MprAdminAcceptReauthenticationEx, rras.mpradminacceptreauthenticationex
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - MprAdminAcceptReauthenticationEx
 - mprapi/MprAdminAcceptReauthenticationEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mprapi.h
api_name:
 - MprAdminAcceptReauthenticationEx
---

# MprAdminAcceptReauthenticationEx function


## -description

Remote Access Service (RAS) calls the 
<b>MprAdminAcceptReauthenticationEx</b> function whenever the quarantine state  
of the client changes. <b>MprAdminAcceptReauthenticationEx</b> determines whether the user is allowed to reauthenticate and connect after the quarantine state has changed.

## -parameters

### -param pRasConn [in]

A pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure that describes this connection.

## -returns

If 
<b>MprAdminAcceptReauthenticationEx</b> accepts the connection, the return value should be <b>TRUE</b>.

If 
<b>MprAdminAcceptReauthenticationEx</b> rejects the connection, the return value should be <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptreauthentication">MprAdminAcceptReauthentication</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>