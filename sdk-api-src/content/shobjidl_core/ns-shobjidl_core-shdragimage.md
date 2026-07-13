---
UID: NS:shobjidl_core.SHDRAGIMAGE
title: SHDRAGIMAGE (shobjidl_core.h)
description: Contains the information needed to create a drag image.
helpviewer_keywords: ["*LPSHDRAGIMAGE","LPSHDRAGIMAGE","LPSHDRAGIMAGE structure pointer [Windows Shell]","SHDRAGIMAGE","SHDRAGIMAGE structure [Windows Shell]","_win32_SHDRAGIMAGE_str","shell.SHDRAGIMAGE_str","shobjidl_core/LPSHDRAGIMAGE","shobjidl_core/SHDRAGIMAGE"]
old-location: shell\SHDRAGIMAGE_str.htm
tech.root: shell
ms.assetid: e0dd76b2-fd5c-41e8-b540-db90a2f0dcec
ms.date: 12/05/2018
ms.keywords: '*LPSHDRAGIMAGE, LPSHDRAGIMAGE, LPSHDRAGIMAGE structure pointer [Windows Shell], SHDRAGIMAGE, SHDRAGIMAGE structure [Windows Shell], _win32_SHDRAGIMAGE_str, shell.SHDRAGIMAGE_str, shobjidl_core/LPSHDRAGIMAGE, shobjidl_core/SHDRAGIMAGE'
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
targetos: Windows
req.typenames: SHDRAGIMAGE, *LPSHDRAGIMAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHDRAGIMAGE
 - shobjidl_core/SHDRAGIMAGE
 - LPSHDRAGIMAGE
 - shobjidl_core/LPSHDRAGIMAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SHDRAGIMAGE
---

# SHDRAGIMAGE structure


## -description

Contains the information needed to create a drag image.

## -struct-fields

### -field sizeDragImage

Type: <b><a href="/windows/win32/api/windef/ns-windef-size">SIZE</a></b>

A <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure with the length and width of the drag image.

### -field ptOffset

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that specifies the location of the cursor within the drag image. The structure should contain the offset from the upper-left corner of the drag image to the location of the cursor.

### -field hbmpDragImage

Type: <b>HBITMAP</b>

The drag image's bitmap handle.

### -field crColorKey

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

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

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap">IDragSourceHelper::InitializeFromBitmap</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow">IDragSourceHelper::InitializeFromWindow</a>