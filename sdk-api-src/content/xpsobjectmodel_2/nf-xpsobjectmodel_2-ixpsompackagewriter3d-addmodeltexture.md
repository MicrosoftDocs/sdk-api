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

# IXpsOMPackageWriter3D::AddModelTexture


## -description


Creates a new 3D model texture from the specified texture part and stream.


## -parameters




### -param texturePartName [in]

The Open Package Convention (OPC)  name of the texture part. This part is added to the package and becomes a relationship target of the model part.


### -param textureData [in]

A readable stream which holds 3D model texture. When calling this method, you must provide PNG or JPEG data.


## -returns



Returns the appropriate HRESULT error code.




## -remarks



Each time this method is called, it creates a new part with a specified name, content and hardcoded content type “application/vnd.ms-package.3dmanufacturing-3dmodeltexture”. That part is linked from the model part with relationship type “http://schemas.microsoft.com/3dmanufacturing/2013/01/3dmodeltexture”. 




## -see-also




<a href="https://msdn.microsoft.com/2F3E0529-7E2B-4BCD-AE8F-D0F3259D1A48">IXpsOMPackageWriter3D</a>
 

 

