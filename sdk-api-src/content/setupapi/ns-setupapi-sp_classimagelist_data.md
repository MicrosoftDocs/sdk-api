---
UID: NS:setupapi._SP_CLASSIMAGELIST_DATA
title: SP_CLASSIMAGELIST_DATA (setupapi.h)
author: windows-sdk-content
description: An SP_CLASSIMAGELIST_DATA structure describes a class image list.
old-location: devinst\sp_classimagelist_data.htm
tech.root: devinst
ms.assetid: 89ed9dbd-3c5e-43ff-bbd0-fd6cc8c6e6ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSP_CLASSIMAGELIST_DATA, PSP_CLASSIMAGELIST_DATA, PSP_CLASSIMAGELIST_DATA structure pointer [Device and Driver Installation], SP_CLASSIMAGELIST_DATA, SP_CLASSIMAGELIST_DATA structure [Device and Driver Installation], devinst.sp_classimagelist_data, di-struct_2d2e73bd-5f18-49d1-96ad-639bc0ad658e.xml, setupapi/PSP_CLASSIMAGELIST_DATA, setupapi/SP_CLASSIMAGELIST_DATA"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: SP_CLASSIMAGELIST_DATA, *PSP_CLASSIMAGELIST_DATA
req.redist: 
ms.custom: 19H1
---

# SP_CLASSIMAGELIST_DATA structure


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




<a href="https://msdn.microsoft.com/47ccc16c-b061-489b-b534-5b5929c5d010">SetupDiDestroyClassImageList</a>



<a href="https://msdn.microsoft.com/56c17b9a-d516-4903-90fc-efac22e1f50d">SetupDiGetClassImageIndex</a>



<a href="https://msdn.microsoft.com/d6b84403-9284-4fba-a419-a013cf68ea1e">SetupDiGetClassImageList</a>
 

 

