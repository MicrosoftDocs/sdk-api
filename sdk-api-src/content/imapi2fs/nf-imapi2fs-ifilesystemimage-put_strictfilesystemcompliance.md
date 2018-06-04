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

# IFileSystemImage::put_StrictFileSystemCompliance


## -description


Determines the compliance level for creating and developing the file-system image.


## -parameters




### -param newVal [in]

Set to VARIANT_TRUE to create the file system images in strict compliance with applicable standards.  You can specify VARIANT_TRUE only when the file system image is empty.

Set to VARIANT_FALSE to relax the compliance standards to be compatible with IMAPI version 1.0.

The default is VARIANT_FALSE.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



If this property is VARIANT_TRUE and a method requests an action that violates one of the file system constraints, an exception is thrown.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/07139ef3-ffd5-4035-afa9-6212808a6fbc">IFileSystemImage::get_StrictFileSystemCompliance</a>
 

 

