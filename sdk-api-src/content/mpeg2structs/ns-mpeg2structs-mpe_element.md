---
UID: NS:mpeg2structs._MPE_ELEMENT
title: MPE_ELEMENT (mpeg2structs.h)
description: The MPE_ELEMENT structure contains information from a multi-protocol encapsulation (MPE) element.
helpviewer_keywords: ["*PMPE_ELEMENT","MPE_ELEMENT","MPE_ELEMENT structure [Microsoft TV Technologies]","PMPE_ELEMENT","PMPE_ELEMENT structure pointer [Microsoft TV Technologies]","mpeg2structs/MPE_ELEMENT","mpeg2structs/PMPE_ELEMENT","mstv.mpe_element"]
old-location: mstv\mpe_element.htm
tech.root: mstv
ms.assetid: 2753160b-de52-4d62-960a-c200c6f5f29a
ms.date: 12/05/2018
ms.keywords: '*PMPE_ELEMENT, MPE_ELEMENT, MPE_ELEMENT structure [Microsoft TV Technologies], PMPE_ELEMENT, PMPE_ELEMENT structure pointer [Microsoft TV Technologies], mpeg2structs/MPE_ELEMENT, mpeg2structs/PMPE_ELEMENT, mstv.mpe_element'
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
targetos: Windows
req.typenames: MPE_ELEMENT, *PMPE_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPE_ELEMENT
 - mpeg2structs/_MPE_ELEMENT
 - PMPE_ELEMENT
 - mpeg2structs/PMPE_ELEMENT
 - MPE_ELEMENT
 - mpeg2structs/MPE_ELEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - MPE_ELEMENT
---

# MPE_ELEMENT structure


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

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>