---
UID: NS:winioctl._CHANGER_ELEMENT
title: "_CHANGER_ELEMENT"
author: windows-sdk-content
description: Represents a changer element.
old-location: base\changer_element_str.htm
old-project: devio
ms.assetid: 96e9803b-16c4-415c-940a-f5df3edff3b3
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: "*PCHANGER_ELEMENT, CHANGER_ELEMENT, CHANGER_ELEMENT structure, PCHANGER_ELEMENT, PCHANGER_ELEMENT structure pointer, _CHANGER_ELEMENT, _win32_changer_element_str, base.changer_element_str, winioctl/CHANGER_ELEMENT, winioctl/PCHANGER_ELEMENT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CHANGER_ELEMENT, *PCHANGER_ELEMENT
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CHANGER_ELEMENT structure


## -description


Represents a changer element.


## -struct-fields




### -field ElementType

The element type. This parameter can be one of the values from the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff553754">ELEMENT_TYPE</a> enumeration type.


### -field ElementAddress

The zero-based address of the element.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551459">CHANGER_ELEMENT_LIST</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553754">ELEMENT_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559419">IOCTL_CHANGER_REINITIALIZE_TRANSPORT</a>
 

 

