---
UID: NS:qossp._FLOWDESCRIPTOR
title: FLOWDESCRIPTOR (qossp.h)
description: The FLOWDESCRIPTOR structure specifies one or more filters for a given FLOWSPEC.
helpviewer_keywords: ["*LPFLOWDESCRIPTOR","*LPFLOWDESCRIPTOR structure [QOS]","FLOWDESCRIPTOR","FLOWDESCRIPTOR structure [QOS]","qos.flowdescriptor","qossp/*LPFLOWDESCRIPTOR","qossp/FLOWDESCRIPTOR"]
old-location: qos\flowdescriptor.htm
tech.root: QOS
ms.assetid: c81a9c68-7124-4a66-9c68-d147d41c0c4d
ms.date: 12/05/2018
ms.keywords: '*LPFLOWDESCRIPTOR, *LPFLOWDESCRIPTOR structure [QOS], FLOWDESCRIPTOR, FLOWDESCRIPTOR structure [QOS], qos.flowdescriptor, qossp/*LPFLOWDESCRIPTOR, qossp/FLOWDESCRIPTOR'
req.header: qossp.h
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
req.typenames: FLOWDESCRIPTOR, *LPFLOWDESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FLOWDESCRIPTOR
 - qossp/_FLOWDESCRIPTOR
 - LPFLOWDESCRIPTOR
 - qossp/LPFLOWDESCRIPTOR
 - FLOWDESCRIPTOR
 - qossp/FLOWDESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - FLOWDESCRIPTOR
---

# FLOWDESCRIPTOR structure


## -description

The <b>FLOWDESCRIPTOR</b> structure specifies one or more filters for a given FLOWSPEC.

## -struct-fields

### -field FlowSpec

Flow specification (FLOWSPEC), provided as a <a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> structure.

### -field NumFilters

Number of filters provided in <b>FilterList</b>.

### -field FilterList

Pointer to a <a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec">RSVP_FILTERSPEC</a> structure containing FILTERSPEC information.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_filterspec">RSVP_FILTERSPEC</a>