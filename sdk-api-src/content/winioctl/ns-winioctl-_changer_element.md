---
UID: NS:winioctl._CHANGER_ELEMENT
title: "_CHANGER_ELEMENT"
author: windows-sdk-content
description: Represents a changer element.
old-location: base\changer_element_str.htm
tech.root: devio
ms.assetid: 96e9803b-16c4-415c-940a-f5df3edff3b3
ms.author: windowssdkdev
ms.date: 08/07/2018
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

# _CHANGER_ELEMENT structure


## -description


Represents a changer element.


## -struct-fields




### -field ElementType

The element type. This parameter can be one of the values from the 
<a href="https://msdn.microsoft.com/b026d0f5-133d-4138-a727-80bf4480bb74">ELEMENT_TYPE</a> enumeration type.


### -field ElementAddress

The zero-based address of the element.


## -see-also




<a href="https://msdn.microsoft.com/cb1fcf78-b36a-4551-8eeb-da58edc80890">CHANGER_ELEMENT_LIST</a>



<a href="https://msdn.microsoft.com/b026d0f5-133d-4138-a727-80bf4480bb74">ELEMENT_TYPE</a>



<a href="https://msdn.microsoft.com/0745ee19-34f3-44c8-a52d-fb47448f0084">IOCTL_CHANGER_REINITIALIZE_TRANSPORT</a>
 

 

