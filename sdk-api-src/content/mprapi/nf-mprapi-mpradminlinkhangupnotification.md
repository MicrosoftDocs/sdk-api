---
UID: NF:mprapi.MprAdminLinkHangupNotification
title: MprAdminLinkHangupNotification function (mprapi.h)
description: RAS calls the MprAdminLinkHangupNotification function whenever a link for a particular connection is dismantled.
helpviewer_keywords: ["MprAdminLinkHangupNotification","MprAdminLinkHangupNotification callback","MprAdminLinkHangupNotification callback function [RAS]","_mpr_mpradminlinkhangupnotification","mprapi/MprAdminLinkHangupNotification","rras.mpradminlinkhangupnotification"]
old-location: rras\mpradminlinkhangupnotification.htm
tech.root: RRAS
ms.assetid: 7f2b30e8-ba1d-4db3-843f-f9eafca47add
ms.date: 12/05/2018
ms.keywords: MprAdminLinkHangupNotification, MprAdminLinkHangupNotification callback, MprAdminLinkHangupNotification callback function [RAS], _mpr_mpradminlinkhangupnotification, mprapi/MprAdminLinkHangupNotification, rras.mpradminlinkhangupnotification
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
 - MprAdminLinkHangupNotification
 - mprapi/MprAdminLinkHangupNotification
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
 - MprAdminLinkHangupNotification
---

# MprAdminLinkHangupNotification function


## -description

RAS calls the 
<b>MprAdminLinkHangupNotification</b> function whenever a link for a particular connection is dismantled.

## -parameters

### -param pRasPort0 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a> structure that describes the port being used by the link.

### -param pRasPort1 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a> structure that describes the port being used by the link.

## -remarks

RAS supports multiple Administration DLLs. RAS calls the multiple implementations of 
<b>MprAdminLinkHangupNotification</b> in the order in which the DLLs are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>.

<b>Windows 2000 Server and earlier:  </b>If RAS does not accept the new link, RAS does not call the 
<b>MprAdminLinkHangupNotification</b> function.

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminLinkHangupNotification</b>. Calls to these functions will not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection">MprAdminAcceptNewConnection</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection2">MprAdminAcceptNewConnection2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewlink">MprAdminAcceptNewLink</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification2">MprAdminConnectionHangupNotification2</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>