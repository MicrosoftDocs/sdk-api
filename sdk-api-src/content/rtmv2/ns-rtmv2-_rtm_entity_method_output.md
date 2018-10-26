---
UID: NS:rtmv2._RTM_ENTITY_METHOD_OUTPUT
title: "_RTM_ENTITY_METHOD_OUTPUT"
author: windows-sdk-content
description: The RTM_ENTITY_METHOD_OUTPUT structure is used to pass information to the calling client when the routing table manager invokes a method.
old-location: rras\rtm_entity_method_output.htm
tech.root: rras
ms.assetid: 9ec05355-a912-4ed0-ace9-8823d333bab5
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: "*PRTM_ENTITY_METHOD_OUTPUT, PRTM_ENTITY_METHOD_OUTPUT, PRTM_ENTITY_METHOD_OUTPUT structure pointer [RAS], RTM_ENTITY_METHOD_OUTPUT, RTM_ENTITY_METHOD_OUTPUT structure [RAS], _RTM_ENTITY_METHOD_OUTPUT, _rtmv2ref_rtm_entity_method_output, rras.rtm_entity_method_output, rtmv2/PRTM_ENTITY_METHOD_OUTPUT, rtmv2/RTM_ENTITY_METHOD_OUTPUT"
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rtmv2.h
api_name:
 - RTM_ENTITY_METHOD_OUTPUT
product: Windows
targetos: Windows
req.typenames: RTM_ENTITY_METHOD_OUTPUT, *PRTM_ENTITY_METHOD_OUTPUT
req.redist: 
---

# _RTM_ENTITY_METHOD_OUTPUT structure


## -description


The 
<b>RTM_ENTITY_METHOD_OUTPUT</b> structure is used to pass information to the calling client when the routing table manager invokes a method.


## -struct-fields




### -field MethodType

Specifies the method identifier.


### -field MethodStatus

Receives the status of the method after execution.


### -field OutputSize

Specifies the size, in bytes, of <b>OutputData</b>.


### -field OutputData

Buffer for data returned by the method.


## -see-also




<a href="https://msdn.microsoft.com/97506565-2fa7-4ff7-b397-7ab712759a5d">RtmInvokeMethod</a>
 

 

