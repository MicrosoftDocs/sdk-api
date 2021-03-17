---
UID: NF:mprapi.MprAdminConnectionHangupNotification
title: MprAdminConnectionHangupNotification function (mprapi.h)
description: Remote Access Service calls the MprAdminConnectionHangupNotification function after the last link for the specified connection has been dismantled.
helpviewer_keywords: ["MprAdminConnectionHangupNotification","MprAdminConnectionHangupNotification callback","MprAdminConnectionHangupNotification callback function [RAS]","_mpr_mpradminconnectionhangupnotification","mprapi/MprAdminConnectionHangupNotification","rras.mpradminconnectionhangupnotification"]
old-location: rras\mpradminconnectionhangupnotification.htm
tech.root: RRAS
ms.assetid: 504ce881-7d06-41d3-a942-0fe27be12bd3
ms.date: 12/05/2018
ms.keywords: MprAdminConnectionHangupNotification, MprAdminConnectionHangupNotification callback, MprAdminConnectionHangupNotification callback function [RAS], _mpr_mpradminconnectionhangupnotification, mprapi/MprAdminConnectionHangupNotification, rras.mpradminconnectionhangupnotification
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
 - MprAdminConnectionHangupNotification
 - mprapi/MprAdminConnectionHangupNotification
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
 - MprAdminConnectionHangupNotification
---

# MprAdminConnectionHangupNotification function


## -description

Remote Access Service calls the 
<b>MprAdminConnectionHangupNotification</b> function after the last link for the specified connection has been dismantled.

## -parameters

### -param pRasConnection0 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a> structure that describes this connection.

### -param pRasConnection1 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a> structure that describes this connection.

## -remarks

RAS supports multiple Administration DLLs. RAS calls the multiple implementations of the 
<b>MprAdminConnectionHangupNotification</b> function in the order in which the DLLs are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>.

<b>Windows 2000 Server and earlier:  </b>If 
<b>MprAdminAcceptNewConnection</b> does not accept the new connection, RAS does not call the 
<b>MprAdminConnectionHangupNotification</b> function.

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminConnectionHangupNotification</b>. Calls to these functions do not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection">MprAdminAcceptNewConnection</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewlink">MprAdminAcceptNewLink</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification2">MprAdminConnectionHangupNotification2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification3">MprAdminConnectionHangupNotification3</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_0">RAS_CONNECTION_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_1">RAS_CONNECTION_1</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>