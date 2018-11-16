---
UID: NS:mpeg2structs._MPE_ELEMENT
title: "_MPE_ELEMENT"
author: windows-sdk-content
description: The MPE_ELEMENT structure contains information from a multi-protocol encapsulation (MPE) element.
old-location: mstv\mpe_element.htm
tech.root: mstv
ms.assetid: 2753160b-de52-4d62-960a-c200c6f5f29a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PMPE_ELEMENT, MPE_ELEMENT, MPE_ELEMENT structure [Microsoft TV Technologies], PMPE_ELEMENT, PMPE_ELEMENT structure pointer [Microsoft TV Technologies], _MPE_ELEMENT, mpeg2structs/MPE_ELEMENT, mpeg2structs/PMPE_ELEMENT, mstv.mpe_element"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mpeg2structs.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - MPE_ELEMENT
product: Windows
targetos: Windows
req.typenames: MPE_ELEMENT, *PMPE_ELEMENT
req.redist: 
---

# _MPE_ELEMENT structure


## -description



The <b>MPE_ELEMENT</b> structure contains information from a multi-protocol encapsulation (MPE) element.




## -struct-fields




### -field pid

Packet identifier (PID).


### -field bComponentTag

Component tag.


### -field pNext

Pointer to the next <b>MPE_ELEMENT</b> structure in the list, or <b>NULL</b> if this element is the end of the list.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

