---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL_ITfFnGetPreferredTouchKeyboardLayout_0001 enumeration


## -description


Elements of the <b>TKBLayoutType</b> enumeration are passed by an IME in a call to <a href="https://msdn.microsoft.com/03C14744-A4A3-4C62-8E7F-CDCC638BBCA1">ITfFnGetPreferredTouchKeyboardLayout::GetLayout</a> to specify the type of layout.




## -enum-fields




### -field TKBLT_UNDEFINED

 Undefined. If specified, it will cause the layout to fallback to a classic layout.


### -field TKBLT_CLASSIC

The touch keyboard is to use a classic layout.


### -field TKBLT_OPTIMIZED

The touch keyboard is to use a touch-optimized layout.


## -see-also




<a href="https://msdn.microsoft.com/03C14744-A4A3-4C62-8E7F-CDCC638BBCA1">ITfFnGetPreferredTouchKeyboardLayout::GetLayout</a>
 

 

