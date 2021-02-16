---
UID: NS:winioctl._CHANGER_ELEMENT
title: CHANGER_ELEMENT
description: Represents a changer element.
helpviewer_keywords: ["*PCHANGER_ELEMENT","CHANGER_ELEMENT","CHANGER_ELEMENT structure","PCHANGER_ELEMENT","PCHANGER_ELEMENT structure pointer","_win32_changer_element_str","base.changer_element_str","winioctl/CHANGER_ELEMENT","winioctl/PCHANGER_ELEMENT"]
old-location: base\changer_element_str.htm
tech.root: base
ms.assetid: 96e9803b-16c4-415c-940a-f5df3edff3b3
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_ELEMENT, CHANGER_ELEMENT, CHANGER_ELEMENT structure, PCHANGER_ELEMENT, PCHANGER_ELEMENT structure pointer, _win32_changer_element_str, base.changer_element_str, winioctl/CHANGER_ELEMENT, winioctl/PCHANGER_ELEMENT'
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: CHANGER_ELEMENT, *PCHANGER_ELEMENT
req.redist: 
f1_keywords:
 - _CHANGER_ELEMENT
 - winioctl/_CHANGER_ELEMENT
 - PCHANGER_ELEMENT
 - winioctl/PCHANGER_ELEMENT
 - CHANGER_ELEMENT
 - winioctl/CHANGER_ELEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - CHANGER_ELEMENT
---

# CHANGER_ELEMENT structure


## -description

Represents a changer element.

## -struct-fields

### -field ElementType

The element type. This parameter can be one of the values from the 
<a href="/windows/desktop/api/winioctl/ne-winioctl-element_type">ELEMENT_TYPE</a> enumeration type.

### -field ElementAddress

The zero-based address of the element.

## -see-also

<a href="/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a>



<a href="/windows/desktop/api/winioctl/ne-winioctl-element_type">ELEMENT_TYPE</a>



<a href="/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_reinitialize_transport">IOCTL_CHANGER_REINITIALIZE_TRANSPORT</a>