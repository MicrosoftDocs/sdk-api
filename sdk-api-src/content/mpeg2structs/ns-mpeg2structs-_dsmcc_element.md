---
UID: NS:mpeg2structs._DSMCC_ELEMENT
title: "_DSMCC_ELEMENT"
author: windows-sdk-content
description: The DSMCC_ELEMENT structure contains information from a DSM-CC element.
old-location: mstv\dsmcc_element.htm
tech.root: MSTV
ms.assetid: 4d556cd8-cac5-4d79-a440-e2b5deddcdf8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PDSMCC_ELEMENT, DSMCC_ELEMENT, DSMCC_ELEMENT structure [Microsoft TV Technologies], PDSMCC_ELEMENT, PDSMCC_ELEMENT structure pointer [Microsoft TV Technologies], _DSMCC_ELEMENT, mpeg2structs/DSMCC_ELEMENT, mpeg2structs/PDSMCC_ELEMENT, mstv.dsmcc_element"
ms.prod: windows
ms.technology: windows-sdk
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
 - DSMCC_ELEMENT
product: Windows
targetos: Windows
req.typenames: DSMCC_ELEMENT, *PDSMCC_ELEMENT
req.redist: 
---

# _DSMCC_ELEMENT structure


## -description



The <b>DSMCC_ELEMENT</b> structure contains information from a DSM-CC element.




## -struct-fields




### -field pid

Packet identifier (PID).


### -field bComponentTag

Component tag.


### -field dwCarouselId

Carousel identifier.


### -field dwTransactionId

Transaction identifier.


### -field pNext

Pointer to the next <b>DSMCC_ELEMENT</b> structure in the list, or <b>NULL</b> if this element is the end of the list.


## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

