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

# DXGI_OUTDUPL_POINTER_SHAPE_INFO structure


## -description


The <b>DXGI_OUTDUPL_POINTER_SHAPE_INFO</b> structure describes information about the cursor shape.


## -struct-fields




### -field Type

A <a href="https://msdn.microsoft.com/A066B6D3-A72A-48A9-BAED-BC3488BD1BC7">DXGI_OUTDUPL_POINTER_SHAPE_TYPE</a>-typed value that specifies the type of cursor shape. 


### -field Width

The width in pixels of the mouse cursor.


### -field Height

The height in scan lines of the mouse cursor.


### -field Pitch

The width in bytes of the mouse cursor.


### -field HotSpot

The position of the cursor's hot spot relative to its upper-left pixel. An application does not use the hot spot when it determines where to draw the cursor shape.


## -remarks



An application draws the cursor shape with the top-left-hand corner drawn at the position that the <b>Position</b> member of the  <a href="https://msdn.microsoft.com/CCD55021-8F67-463D-BA00-46D8B9D22B9A">DXGI_OUTDUPL_POINTER_POSITION</a> structure specifies; the application does not use the hot spot to draw the cursor shape.

An application calls the  <a href="https://msdn.microsoft.com/321FDB62-BF0E-402E-A00B-6F60B7F132AA">IDXGIOutputDuplication::GetFramePointerShape</a> method to retrieve cursor shape information in a  <b>DXGI_OUTDUPL_POINTER_SHAPE_INFO</b> structure.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/321FDB62-BF0E-402E-A00B-6F60B7F132AA">IDXGIOutputDuplication::GetFramePointerShape</a>
 

 

