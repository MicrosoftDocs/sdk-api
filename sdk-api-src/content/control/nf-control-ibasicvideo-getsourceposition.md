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

# IBasicVideo::GetSourcePosition


## -description



The <code>GetSourcePosition</code> method retrieves the position of the source rectangle.




## -parameters




### -param pLeft [out]

Pointer to a variable that receives the x-coordinate, in pixels.


### -param pTop [out]

Pointer to a variable that receives the y-coordinate, in pixels.


### -param pWidth [out]

Pointer to a variable that receives the width, in pixels.


### -param pHeight [out]

Pointer to a variable that receives the height, in pixels.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/1ea64dae-d643-44c1-9026-f9b0dcd25ef1">IBasicVideo::get_SourceLeft</a>, <a href="https://msdn.microsoft.com/87ad3699-5a1b-4fa0-b7bd-5ec87758e9fa">IBasicVideo::get_SourceTop</a>, <a href="https://msdn.microsoft.com/6c6f7e01-5f93-4277-b664-c5be0ea42004">IBasicVideo::get_SourceWidth</a>, and <a href="https://msdn.microsoft.com/3f4e779a-cfa9-496d-a021-d24ae3daa5b3">IBasicVideo::get_SourceHeight</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

