---
UID: NS:setupapi._SP_CLASSIMAGELIST_DATA
title: "_SP_CLASSIMAGELIST_DATA"
author: windows-sdk-content
description: An SP_CLASSIMAGELIST_DATA structure describes a class image list.
old-location: devinst\sp_classimagelist_data.htm
old-project: devinst
ms.assetid: 89ed9dbd-3c5e-43ff-bbd0-fd6cc8c6e6ab
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: "*PSP_CLASSIMAGELIST_DATA, PSP_CLASSIMAGELIST_DATA, PSP_CLASSIMAGELIST_DATA structure pointer [Device and Driver Installation], SP_CLASSIMAGELIST_DATA, SP_CLASSIMAGELIST_DATA structure [Device and Driver Installation], _SP_CLASSIMAGELIST_DATA, devinst.sp_classimagelist_data, di-struct_2d2e73bd-5f18-49d1-96ad-639bc0ad658e.xml, setupapi/PSP_CLASSIMAGELIST_DATA, setupapi/SP_CLASSIMAGELIST_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
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
tech.root: 
req.typenames: SP_CLASSIMAGELIST_DATA, *PSP_CLASSIMAGELIST_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_CLASSIMAGELIST_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SP_CLASSIMAGELIST_DATA structure


## -description


An SP_CLASSIMAGELIST_DATA structure describes a class image list.


## -struct-fields




### -field cbSize

The size, in bytes, of the SP_CLASSIMAGE_DATA structure. 


### -field ImageList

A handle to the class image list.


### -field Reserved

Reserved. For internal use only.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550995">SetupDiDestroyClassImageList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551074">SetupDiGetClassImageIndex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551080">SetupDiGetClassImageList</a>
 

 

