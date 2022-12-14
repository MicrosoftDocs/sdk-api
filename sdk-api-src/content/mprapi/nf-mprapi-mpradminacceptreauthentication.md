---
UID: NF:mprapi.MprAdminAcceptReauthentication
title: MprAdminAcceptReauthentication function (mprapi.h)
description: Remote Access Service calls the MprAdminAcceptReauthentication function whenever the quarantine state of the client changes.
helpviewer_keywords: ["MprAdminAcceptReauthentication","MprAdminAcceptReauthentication callback","MprAdminAcceptReauthentication callback function [RAS]","mprapi/MprAdminAcceptReauthentication","rras.mpradminacceptreauthentication"]
old-location: rras\mpradminacceptreauthentication.htm
tech.root: RRAS
ms.assetid: 58fea0ca-b7c1-4d32-bcfc-10b41e101f30
ms.date: 12/05/2018
ms.keywords: MprAdminAcceptReauthentication, MprAdminAcceptReauthentication callback, MprAdminAcceptReauthentication callback function [RAS], mprapi/MprAdminAcceptReauthentication, rras.mpradminacceptreauthentication
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MprAdminAcceptReauthentication
 - mprapi/MprAdminAcceptReauthentication
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
 - MprAdminAcceptReauthentication
---

# MprAdminAcceptReauthentication function


## -description

Remote Access Service calls the 
<b>MprAdminAcceptReauthentication</b> function whenever the quarantine state  
of the client changes. <b>MprAdminAcceptReauthentication</b> determines whether the user is allowed to reauthenticate and connect after the quarantine state has changed.

The quarantine state of a connection is determined by the Network Access Protection (NAP) agent, and is stored in the <b>rasQuarState</b> member of the <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a> structure.

## -parameters

### -param pRasConnection0 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a> structure that describes this connection.

### -param pRasConnection1 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a> structure that describes this connection.

### -param pRasConnection2 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a> structure that describes this connection.

### -param pRasConnection3 [in]

Pointer to a 
 <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a> structure that describes this connection.

## -returns

If 
<b>MprAdminAcceptReauthentication</b> accepts the connection, the return value should be <b>TRUE</b>.

If 
<b>MprAdminAcceptReauthentication</b> rejects the connection, the return value should be <b>FALSE</b>.

## -remarks

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminAcceptReauthentication</b>. Calls to these functions do not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>