---
UID: NS:rtmv2._RTM_ENTITY_METHOD_INPUT
title: "_RTM_ENTITY_METHOD_INPUT"
author: windows-driver-content
description: The RTM_ENTITY_METHOD_INPUT structure is used to pass information to a client when invoking its method.
old-location: rras\rtm_entity_method_input.htm
old-project: RRAS
ms.assetid: 1f900e85-c522-47c9-bfc8-5a1c1d01ab78
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PRTM_ENTITY_METHOD_INPUT, PRTM_ENTITY_METHOD_INPUT, PRTM_ENTITY_METHOD_INPUT structure pointer [RAS], RTM_ENTITY_METHOD_INPUT, RTM_ENTITY_METHOD_INPUT structure [RAS], _RTM_ENTITY_METHOD_INPUT, _rtmv2ref_rtm_entity_method_input, rras.rtm_entity_method_input, rtmv2/PRTM_ENTITY_METHOD_INPUT, rtmv2/RTM_ENTITY_METHOD_INPUT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: RTM_ENTITY_METHOD_INPUT, *PRTM_ENTITY_METHOD_INPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rtmv2.h
api_name:
-	RTM_ENTITY_METHOD_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _RTM_ENTITY_METHOD_INPUT structure


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




<a href="https://msdn.microsoft.com/97506565-2fa7-4ff7-b397-7ab712759a5d">RtmInvokeMethod</a>
 

 

