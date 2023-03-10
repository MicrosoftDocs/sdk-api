---
UID: NS:lpmapi.IS_FLOWSPEC
title: IS_FLOWSPEC (lpmapi.h)
description: The IS_FLOWSPEC structure stores an Integrated Services FLOWSPEC object.
helpviewer_keywords: ["IS_FLOWSPEC","IS_FLOWSPEC structure [QOS]","lpmapi/IS_FLOWSPEC","qos.is_flowspec"]
old-location: qos\is_flowspec.htm
tech.root: QOS
ms.assetid: 1e0cd196-f53c-4d68-a287-7a98b7215d6d
ms.date: 12/05/2018
ms.keywords: IS_FLOWSPEC, IS_FLOWSPEC structure [QOS], lpmapi/IS_FLOWSPEC, qos.is_flowspec
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
req.typenames: IS_FLOWSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IS_FLOWSPEC
 - lpmapi/IS_FLOWSPEC
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
 - IS_FLOWSPEC
---

# IS_FLOWSPEC structure


## -description

The 
<b>IS_FLOWSPEC</b> structure stores an Integrated Services FLOWSPEC object.

## -struct-fields

### -field flow_header

General information and length information for the Integrated Services flowspec object (this structure), expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.

### -field flow_body

FLOWSPEC object data, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservflowspec">IntServFlowSpec</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservflowspec">IntServFlowSpec</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>

