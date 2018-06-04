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

# SHDRAGIMAGE structure


## -description


Contains the information needed to create a drag image.


## -struct-fields




### -field sizeDragImage

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure with the length and width of the drag image.


### -field ptOffset

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that specifies the location of the cursor within the drag image. The structure should contain the offset from the upper-left corner of the drag image to the location of the cursor.


### -field hbmpDragImage

Type: <b>HBITMAP</b>

The drag image's bitmap handle.


### -field crColorKey

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

The color used by the control to fill the background of the drag image.


## -remarks



In Windows Vista this structure is defined in Shobjidl.idl. Prior to that, it was defined in Shlobj.h.

Use the following procedure to create the drag image.

<ol>
<li>Create a bitmap of the size specified by <b>sizeDragImage</b> with a handle to a device context (HDC) that is compatible with the screen.</li>
<li>Draw the bitmap.</li>
<li>Select the bitmap out of the HDC it was created with.</li>
<li>Destroy the HDC.</li>
<li>Assign the bitmap handle to <b>hbmpDragImage</b>.</li>
</ol>
<div class="alert"><b>Note</b>  Turn off antialiasing when drawing text. Otherwise, artifacts could occur at the edges, between the text color and the color key.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d50be9c9-f407-4386-bb8f-04c849205359">IDragSourceHelper::InitializeFromBitmap</a>



<a href="https://msdn.microsoft.com/0bcdfe92-cec0-44f3-a345-5b560d52fae9">IDragSourceHelper::InitializeFromWindow</a>
 

 

