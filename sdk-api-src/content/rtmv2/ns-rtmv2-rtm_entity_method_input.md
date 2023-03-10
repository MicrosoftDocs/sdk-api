---
UID: NS:rtmv2._RTM_ENTITY_METHOD_INPUT
title: RTM_ENTITY_METHOD_INPUT (rtmv2.h)
description: The RTM_ENTITY_METHOD_INPUT structure is used to pass information to a client when invoking its method.
helpviewer_keywords: ["*PRTM_ENTITY_METHOD_INPUT","PRTM_ENTITY_METHOD_INPUT","PRTM_ENTITY_METHOD_INPUT structure pointer [RAS]","RTM_ENTITY_METHOD_INPUT","RTM_ENTITY_METHOD_INPUT structure [RAS]","_rtmv2ref_rtm_entity_method_input","rras.rtm_entity_method_input","rtmv2/PRTM_ENTITY_METHOD_INPUT","rtmv2/RTM_ENTITY_METHOD_INPUT"]
old-location: rras\rtm_entity_method_input.htm
tech.root: RRAS
ms.assetid: 1f900e85-c522-47c9-bfc8-5a1c1d01ab78
ms.date: 12/05/2018
ms.keywords: '*PRTM_ENTITY_METHOD_INPUT, PRTM_ENTITY_METHOD_INPUT, PRTM_ENTITY_METHOD_INPUT structure pointer [RAS], RTM_ENTITY_METHOD_INPUT, RTM_ENTITY_METHOD_INPUT structure [RAS], _rtmv2ref_rtm_entity_method_input, rras.rtm_entity_method_input, rtmv2/PRTM_ENTITY_METHOD_INPUT, rtmv2/RTM_ENTITY_METHOD_INPUT'
req.header: rtmv2.h
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
req.typenames: RTM_ENTITY_METHOD_INPUT, *PRTM_ENTITY_METHOD_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTM_ENTITY_METHOD_INPUT
 - rtmv2/_RTM_ENTITY_METHOD_INPUT
 - PRTM_ENTITY_METHOD_INPUT
 - rtmv2/PRTM_ENTITY_METHOD_INPUT
 - RTM_ENTITY_METHOD_INPUT
 - rtmv2/RTM_ENTITY_METHOD_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_ENTITY_METHOD_INPUT
---

# RTM_ENTITY_METHOD_INPUT structure


## -description

The 
<b>RTM_ENTITY_METHOD_INPUT</b> structure is used to pass information to a client when invoking its method.

## -struct-fields

### -field MethodType

Specifies the method.

### -field InputSize

Specifies the size, in bytes, of <b>InputData</b>.

### -field InputData

Buffer for input data for the method.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtminvokemethod">RtmInvokeMethod</a>