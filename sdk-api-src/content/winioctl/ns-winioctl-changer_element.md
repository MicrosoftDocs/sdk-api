---
UID: NS:winioctl._CHANGER_ELEMENT
title: CHANGER_ELEMENT
author: windows-sdk-content
description: Represents a changer element.
old-location: base\changer_element_str.htm
tech.root: devio
ms.assetid: 96e9803b-16c4-415c-940a-f5df3edff3b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PCHANGER_ELEMENT, CHANGER_ELEMENT, CHANGER_ELEMENT structure, PCHANGER_ELEMENT, PCHANGER_ELEMENT structure pointer, _win32_changer_element_str, base.changer_element_str, winioctl/CHANGER_ELEMENT, winioctl/PCHANGER_ELEMENT'
ms.topic: struct
f1_keywords:
- winioctl/CHANGER_ELEMENT
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinIoCtl.h
api_name:
- CHANGER_ELEMENT
product: Windows
targetos: Windows
req.typenames: CHANGER_ELEMENT, *PCHANGER_ELEMENT
req.redist: 
---

# CHANGER_ELEMENT structure


## -description


Represents a changer element.


## -struct-fields




### -field ElementType

The element type. This parameter can be one of the values from the 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-element_type">ELEMENT_TYPE</a> enumeration type.


### -field ElementAddress

The zero-based address of the element.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-changer_element_list">CHANGER_ELEMENT_LIST</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ne-winioctl-element_type">ELEMENT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-ioctl_changer_reinitialize_transport">IOCTL_CHANGER_REINITIALIZE_TRANSPORT</a>
 

 

