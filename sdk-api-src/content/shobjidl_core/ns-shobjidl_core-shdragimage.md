---
UID: NS:shobjidl_core.SHDRAGIMAGE
title: SHDRAGIMAGE
author: windows-sdk-content
description: Contains the information needed to create a drag image.
old-location: shell\SHDRAGIMAGE_str.htm
tech.root: shell
ms.assetid: e0dd76b2-fd5c-41e8-b540-db90a2f0dcec
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPSHDRAGIMAGE, LPSHDRAGIMAGE, LPSHDRAGIMAGE structure pointer [Windows Shell], SHDRAGIMAGE, SHDRAGIMAGE structure [Windows Shell], _win32_SHDRAGIMAGE_str, shell.SHDRAGIMAGE_str, shobjidl_core/LPSHDRAGIMAGE, shobjidl_core/SHDRAGIMAGE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP3, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl_core.h
api_name:
 - SHDRAGIMAGE
product: Windows
targetos: Windows
req.typenames: SHDRAGIMAGE, *LPSHDRAGIMAGE
req.redist: 
---

# SHDRAGIMAGE structure


## -description


Contains the information needed to create a drag image.


## -struct-fields




### -field sizeDragImage

Type: <b><a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a></b>

A <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure with the length and width of the drag image.


### -field ptOffset

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that specifies the location of the cursor within the drag image. The structure should contain the offset from the upper-left corner of the drag image to the location of the cursor.


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
 

 

