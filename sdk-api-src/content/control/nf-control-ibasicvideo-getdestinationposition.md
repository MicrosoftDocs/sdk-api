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

# IBasicVideo::GetDestinationPosition


## -description



The <code>GetDestinationPosition</code> method retrieves the position of the destination rectangle.




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



This method has the same effect as individually calling the <a href="https://msdn.microsoft.com/578f5bbd-23b0-4100-a1d8-0987381fd56f">IBasicVideo::get_DestinationLeft</a>, <a href="https://msdn.microsoft.com/79690655-ac84-4119-9d87-799990424f00">IBasicVideo::get_DestinationTop</a>, <a href="https://msdn.microsoft.com/6e27bb57-ca88-4478-86b8-250a69f5fc78">IBasicVideo::get_DestinationWidth</a>, and <a href="https://msdn.microsoft.com/21d6c74a-2adb-4015-b0df-5acb26c22212">IBasicVideo::get_DestinationHeight</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14f45bdc-2271-459d-b165-c860c8fc3e0b">IBasicVideo Interface</a>
 

 

