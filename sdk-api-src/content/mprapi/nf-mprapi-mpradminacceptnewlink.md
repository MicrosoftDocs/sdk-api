---
UID: NF:mprapi.MprAdminAcceptNewLink
title: MprAdminAcceptNewLink function (mprapi.h)
description: Remote Access Service (RAS) calls the MprAdminAcceptNewLink function each time a link is created for a particular connection.
helpviewer_keywords: ["MprAdminAcceptNewLink","MprAdminAcceptNewLink callback","MprAdminAcceptNewLink callback function [RAS]","_mpr_mpradminacceptnewlink","mprapi/MprAdminAcceptNewLink","rras.mpradminacceptnewlink"]
old-location: rras\mpradminacceptnewlink.htm
tech.root: RRAS
ms.assetid: a4cbca7d-a8b0-4396-9201-648bcca6a8c8
ms.date: 12/05/2018
ms.keywords: MprAdminAcceptNewLink, MprAdminAcceptNewLink callback, MprAdminAcceptNewLink callback function [RAS], _mpr_mpradminacceptnewlink, mprapi/MprAdminAcceptNewLink, rras.mpradminacceptnewlink
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
 - MprAdminAcceptNewLink
 - mprapi/MprAdminAcceptNewLink
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
 - MprAdminAcceptNewLink
---

# MprAdminAcceptNewLink function


## -description

Remote Access Service (RAS) calls the 
<b>MprAdminAcceptNewLink</b> function each time a link is created for a particular connection. RAS calls this function once immediately after 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection">MprAdminAcceptNewConnection</a> returns, and an additional time for every new link that is to be used with the connection.

## -parameters

### -param pRasPort0 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a> structure that describes the port being used by the link.

### -param pRasPort1 [in]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a> structure that describes the port being used by the link.

## -returns

If RAS should accept the new link, the return value should be <b>TRUE</b>.

If RAS should not accept the new link, the return value should be <b>FALSE</b>.

## -remarks

RAS supports multiple Administration DLLs. RAS calls the multiple implementations of 
<b>MprAdminAcceptNewLink</b> in the order in which the DLLs are listed in the 
<a href="/windows/desktop/RRAS/ras-administration-dll-registry-setup">registry</a>. The remote-access user is allowed to connect only if the implementation of 
<b>MprAdminAcceptNewLink</b> in each of the DLLs accepts the connection. In other words, every DLL must accept the link in order for the link to be established.

<b>Windows 2000 Server and earlier:  </b>If RAS does not accept the new link, RAS does not call the 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminlinkhangupnotification">MprAdminLinkHangupNotification</a> function.

Do not call any of the 
<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a> or 
<a href="/windows/desktop/RRAS/ras-user-administration-functions">RAS User Administration Functions</a> from inside 
<b>MprAdminAcceptNewLink</b>. Calls to these functions do not return when made from within a callout function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminacceptnewconnection">MprAdminAcceptNewConnection</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminconnectionhangupnotification">MprAdminConnectionHangupNotification</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminlinkhangupnotification">MprAdminLinkHangupNotification</a>



<a href="/windows/desktop/RRAS/ras-administration-dll">RAS Administration DLL</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_0">RAS_PORT_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_port_1">RAS_PORT_1</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>