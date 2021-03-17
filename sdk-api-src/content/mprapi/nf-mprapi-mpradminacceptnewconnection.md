---
UID: NF:mprapi.MprAdminAcceptNewConnection
title: MprAdminAcceptNewConnection function (mprapi.h)
description: Remote Access Service calls the MprAdminAcceptNewConnection function each time a new user dials in and successfully completes RAS authentication. MprAdminAcceptNewConnection determines whether the user is allowed to connect.
helpviewer_keywords: ["MprAdminAcceptNewConnection","MprAdminAcceptNewConnection callback","MprAdminAcceptNewConnection callback function [RAS]","_mpr_mpradminacceptnewconnection","mprapi/MprAdminAcceptNewConnection","rras.mpradminacceptnewconnection"]
old-location: rras\mpradminacceptnewconnection.htm
tech.root: RRAS
ms.assetid: 6ca7fe28-53e1-49e0-ab3c-4e8e4343c88c
ms.date: 12/05/2018
ms.keywords: MprAdminAcceptNewConnection, MprAdminAcceptNewConnection callback, MprAdminAcceptNewConnection callback function [RAS], _mpr_mpradminacceptnewconnection, mprapi/MprAdminAcceptNewConnection, rras.mpradminacceptnewconnection
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - MprAdminAcceptNewConnection
 - mprapi/MprAdminAcceptNewConnection
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
 - MprAdminAcceptNewConnection
---

# MprAdminAcceptNewConnection function


## -description

Remote Access Service calls the 
<b>MprAdminAcceptNewConnection</b> function each time a new user dials in and successfully completes RAS authentication. 
<b>MprAdminAcceptNewConnection</b> determines whether the user is allowed to connect.

## -parameters

### -param pRasConnection0 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a> structure that describes this connection.

### -param pRasConnection1 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a> structure that describes this connection.

## -returns

If 
<b>MprAdminAcceptNewConnection</b> accepts the connection, the return value should be <b>TRUE</b>.

If 
<b>MprAdminAcceptNewConnection</b> rejects the connection, the return value should be <b>FALSE</b>.

## -remarks

RAS supports multiple Administration DLLs. RAS calls the multiple implementations of the 
<b>MprAdminAcceptNewConnection</b> function in the order in which the DLLs are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>. The remote-access user is allowed to connect only if the implementation of 
<b>MprAdminAcceptNewConnection</b> in each of the DLLs accepts the connection. In other words, every DLL must accept the connection in order for the user to be allowed to connect.

<b>Windows 2000 Server and earlier:  </b>If 
<b>MprAdminAcceptNewConnection</b> does not accept the new connection, RAS does not call the 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a> function.

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminAcceptNewConnection</b>. Calls to these functions do not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection2">MprAdminAcceptNewConnection2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection3">MprAdminAcceptNewConnection3</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification2">MprAdminConnectionHangupNotification2</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>