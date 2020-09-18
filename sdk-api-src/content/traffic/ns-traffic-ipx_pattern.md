---
UID: NS:traffic._IPX_PATTERN
title: IPX_PATTERN (traffic.h)
description: The IPX_PATTERN structure applies a specific pattern or corresponding mask for the IPX protocol. The IPX_PATTERN structure designation is used by the traffic control interface in the application of packet filters.
helpviewer_keywords: ["*PIPX_PATTERN","*PIPX_PATTERN structure [QOS]","IPX_PATTERN","IPX_PATTERN structure [QOS]","qos.ipx_pattern","traffic/*PIPX_PATTERN","traffic/IPX_PATTERN"]
old-location: qos\ipx_pattern.htm
tech.root: QOS
ms.assetid: bbb5466c-3ec4-48a7-a50e-4859d074d001
ms.date: 12/05/2018
ms.keywords: '*PIPX_PATTERN, *PIPX_PATTERN structure [QOS], IPX_PATTERN, IPX_PATTERN structure [QOS], qos.ipx_pattern, traffic/*PIPX_PATTERN, traffic/IPX_PATTERN'
req.header: traffic.h
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
req.typenames: IPX_PATTERN, *PIPX_PATTERN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPX_PATTERN
 - traffic/_IPX_PATTERN
 - PIPX_PATTERN
 - traffic/PIPX_PATTERN
 - IPX_PATTERN
 - traffic/IPX_PATTERN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Traffic.h
api_name:
 - IPX_PATTERN
---

# IPX_PATTERN structure


## -description

The <b>IPX_PATTERN</b> structure applies a specific pattern or corresponding mask for the IPX protocol. The 
<b>IPX_PATTERN</b> structure designation is used by the traffic control interface in the application of packet filters.

## -struct-fields

### -field Src

### -field Src.NetworkAddress

### -field Src.NodeAddress

### -field Src.Socket

### -field Dest

### -field Src, Dest

Structure used to contain source and destination address information for traffic flow.



#### NetworkAddress

IPX network address to which the node belongs.



#### NodeAddress

IPX  node address of the computer.



#### Socket

Socket on which the mask is to be applied.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>