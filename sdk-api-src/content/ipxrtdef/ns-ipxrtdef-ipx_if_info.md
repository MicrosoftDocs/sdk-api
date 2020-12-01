---
UID: NS:ipxrtdef._IPX_IF_INFO
title: IPX_IF_INFO (ipxrtdef.h)
description: The IPX_IF_INFO structure stores information for an IPX interface.
helpviewer_keywords: ["*PIPX_IF_INFO","IPX_IF_INFO","IPX_IF_INFO structure [RAS]","PIPX_IF_INFO","PIPX_IF_INFO structure pointer [RAS]","_mpr_ipx_if_info","ipxrtdef/IPX_IF_INFO","ipxrtdef/PIPX_IF_INFO","rras.ipx_if_info"]
old-location: rras\ipx_if_info.htm
tech.root: RRAS
ms.assetid: f1c07033-dbfa-4bbe-b275-f5bfc629b2d7
ms.date: 12/05/2018
ms.keywords: '*PIPX_IF_INFO, IPX_IF_INFO, IPX_IF_INFO structure [RAS], PIPX_IF_INFO, PIPX_IF_INFO structure pointer [RAS], _mpr_ipx_if_info, ipxrtdef/IPX_IF_INFO, ipxrtdef/PIPX_IF_INFO, rras.ipx_if_info'
req.header: ipxrtdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: IPX_IF_INFO, *PIPX_IF_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPX_IF_INFO
 - ipxrtdef/_IPX_IF_INFO
 - PIPX_IF_INFO
 - ipxrtdef/PIPX_IF_INFO
 - IPX_IF_INFO
 - ipxrtdef/IPX_IF_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipxrtdef.h
api_name:
 - IPX_IF_INFO
---

# IPX_IF_INFO structure


## -description

The 
<b>IPX_IF_INFO</b> structure stores information for an IPX interface.

## -struct-fields

### -field AdminState

Specifies the administrative state of the interface.

### -field NetbiosAccept

Specifies whether to accept NetBIOS broadcast packets.

### -field NetbiosDeliver

Specifies whether to deliver NetBIOS broadcast packets

## -see-also

<a href="/windows/desktop/api/ipxrtdef/ns-ipxrtdef-ipxwan_if_info">IPXWAN_IF_INFO</a>