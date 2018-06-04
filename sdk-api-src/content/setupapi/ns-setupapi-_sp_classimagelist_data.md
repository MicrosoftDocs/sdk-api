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
 

 

