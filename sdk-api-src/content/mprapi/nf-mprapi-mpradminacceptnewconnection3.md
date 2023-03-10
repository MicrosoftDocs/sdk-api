---
UID: NF:mprapi.MprAdminAcceptNewConnection3
title: MprAdminAcceptNewConnection3 function (mprapi.h)
description: Remote Access Service calls the MprAdminAcceptNewConnection3 function each time a new user dials in and successfully completes RAS authentication. MprAdminAcceptNewConnection3 determines whether the user is allowed to connect.
helpviewer_keywords: ["MprAdminAcceptNewConnection3","MprAdminAcceptNewConnection3 callback","MprAdminAcceptNewConnection3 callback function [RAS]","mprapi/MprAdminAcceptNewConnection3","rras.mpradminacceptnewconnection3"]
old-location: rras\mpradminacceptnewconnection3.htm
tech.root: RRAS
ms.assetid: c457b972-e326-4c6d-b146-f6ce4e18e3ea
ms.date: 12/05/2018
ms.keywords: MprAdminAcceptNewConnection3, MprAdminAcceptNewConnection3 callback, MprAdminAcceptNewConnection3 callback function [RAS], mprapi/MprAdminAcceptNewConnection3, rras.mpradminacceptnewconnection3
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
 - MprAdminAcceptNewConnection3
 - mprapi/MprAdminAcceptNewConnection3
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
 - MprAdminAcceptNewConnection3
---

# MprAdminAcceptNewConnection3 function


## -description

Remote Access Service calls the 
<b>MprAdminAcceptNewConnection3</b> function each time a new user dials in and successfully completes RAS authentication. 
<b>MprAdminAcceptNewConnection3</b> determines whether the user is allowed to connect.

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
<b>MprAdminAcceptNewConnection3</b> accepts the connection, the return value should be <b>TRUE</b>.

If 
<b>MprAdminAcceptNewConnection3</b> rejects the connection, the return value should be <b>FALSE</b>.

## -remarks

RAS supports multiple Administration DLLs. RAS calls the multiple implementations of the 
<b>MprAdminAcceptNewConnection3</b> function in the order in which the DLLs are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>. The remote-access user is allowed to connect only if the implementation of 
<b>MprAdminAcceptNewConnection3</b> in each of the DLLs accepts the connection. In other words, every DLL must accept the connection in order for the user to be allowed to connect.

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminAcceptNewConnection3</b>. Calls to these functions do not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection">MprAdminAcceptNewConnection</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection2">MprAdminAcceptNewConnection2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification2">MprAdminConnectionHangupNotification2</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>