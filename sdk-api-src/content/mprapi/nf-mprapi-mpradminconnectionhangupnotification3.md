---
UID: NF:mprapi.MprAdminConnectionHangupNotification3
title: MprAdminConnectionHangupNotification3 function (mprapi.h)
description: Remote Access Service calls the MprAdminConnectionHangupNotification3 function after the last link for the specified connection has been dismantled.
helpviewer_keywords: ["MprAdminConnectionHangupNotification3","MprAdminConnectionHangupNotification3 callback","MprAdminConnectionHangupNotification3 callback function [RAS]","mprapi/MprAdminConnectionHangupNotification3","rras.mpradminconnectionhangupnotification3"]
old-location: rras\mpradminconnectionhangupnotification3.htm
tech.root: RRAS
ms.assetid: 8c31d345-8f57-47f5-a021-e399f7ccca5d
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionHangupNotification3, MprAdminConnectionHangupNotification3 callback, MprAdminConnectionHangupNotification3 callback function [RAS], mprapi/MprAdminConnectionHangupNotification3, rras.mpradminconnectionhangupnotification3
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
 - MprAdminConnectionHangupNotification3
 - mprapi/MprAdminConnectionHangupNotification3
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
 - MprAdminConnectionHangupNotification3
---

# MprAdminConnectionHangupNotification3 function


## -description

Remote Access Service calls the 
<b>MprAdminConnectionHangupNotification3</b> function after the last link for the specified connection has been dismantled.

## -parameters

### -param pRasConnection0 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a> structure that describes this connection.

### -param pRasConnection1 [in]

Pointer to the 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a> structure that describes this connection.

### -param pRasConnection2 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a> structure that describes this connection.

### -param pRasConnection3 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a> structure that describes this connection.

## -remarks

RAS supports multiple Administration DLLs. RAS calls the multiple implementations of the 
<b>MprAdminConnectionHangupNotification3</b> function in the order in which the DLLs are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>.

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminConnectionHangupNotification3</b>. Calls to these functions do not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection3">MprAdminAcceptNewConnection3</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewlink">MprAdminAcceptNewLink</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification2">MprAdminConnectionHangupNotification2</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_2">RAS_CONNECTION_2</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_3">RAS_CONNECTION_3</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>