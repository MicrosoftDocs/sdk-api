---
UID: NS:lpmapi.GenAdspecParams
title: GenAdspecParams (lpmapi.h)
description: The GenAdspecParams structure contains general path characterization parameters.
helpviewer_keywords: ["GenAdspecParams","GenAdspecParams structure [QOS]","lpmapi/GenAdspecParams","qos.genadspecparams"]
old-location: qos\genadspecparams.htm
tech.root: QOS
ms.assetid: 0d980286-bce6-483e-b2a1-117c7280c1c1
ms.date: 12/05/2018
ms.keywords: GenAdspecParams, GenAdspecParams structure [QOS], lpmapi/GenAdspecParams, qos.genadspecparams
req.header: lpmapi.h
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
req.typenames: GenAdspecParams
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GenAdspecParams
 - lpmapi/GenAdspecParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - GenAdspecParams
---

# GenAdspecParams structure


## -description

The 
<b>GenAdspecParams</b> structure contains general path characterization parameters.

## -struct-fields

### -field gen_parm_hdr

General information and length information for the Adspec parameters object (this structure), expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a> structure.

### -field gen_parm_hopcnt_hdr

Parameter header for hop count information associated with the Adspec object, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.

### -field gen_parm_hopcnt

Hop count information parameter.

### -field gen_parm_pathbw_hdr

Parameter header for path bandwidth information associated with the Adspec object, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.

### -field gen_parm_path_bw

Path bandwidth information parameter.

### -field gen_parm_minlat_hdr

Parameter header for minimum latency information associated with the Adspec object, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.

### -field gen_parm_min_latency

Minimum latency information parameter.

### -field gen_parm_compmtu_hdr

Parameter header for composed maximum transmission unit (MTU) information associated with the Adspec object, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a> structure.

### -field gen_parm_composed_MTU

Composed MTU information parameter.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>

