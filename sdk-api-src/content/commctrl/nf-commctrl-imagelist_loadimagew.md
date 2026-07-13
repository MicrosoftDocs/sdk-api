---
UID: NF:commctrl.ImageList_LoadImageW
title: ImageList_LoadImageW function (commctrl.h)
description: Creates an image list from the specified bitmap. (Unicode)
helpviewer_keywords: ["IMAGE_BITMAP", "ImageList_LoadImage", "ImageList_LoadImage function [Windows Controls]", "ImageList_LoadImageW", "LR_CREATEDIBSECTION", "LR_DEFAULTCOLOR", "LR_DEFAULTSIZE", "LR_LOADFROMFILE", "LR_LOADMAP3DCOLORS", "LR_LOADTRANSPARENT", "LR_MONOCHROME", "LR_SHARED", "OBM_ for OEM bitmaps", "OCR_ for OEM cursors", "OIC_ for OEM icons", "_win32_ImageList_LoadImage", "_win32_ImageList_LoadImage_cpp", "commctrl/ImageList_LoadImage", "commctrl/ImageList_LoadImageW", "controls.ImageList_LoadImage", "controls._win32_ImageList_LoadImage"]
old-location: controls\ImageList_LoadImage.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_loadimage.htm
ms.date: 12/05/2018
ms.keywords: IMAGE_BITMAP, ImageList_LoadImage, ImageList_LoadImage function [Windows Controls], ImageList_LoadImageA, ImageList_LoadImageW, LR_CREATEDIBSECTION, LR_DEFAULTCOLOR, LR_DEFAULTSIZE, LR_LOADFROMFILE, LR_LOADMAP3DCOLORS, LR_LOADTRANSPARENT, LR_MONOCHROME, LR_SHARED, OBM_ for OEM bitmaps, OCR_ for OEM cursors, OIC_ for OEM icons, _win32_ImageList_LoadImage, _win32_ImageList_LoadImage_cpp, commctrl/ImageList_LoadImage, commctrl/ImageList_LoadImageA, commctrl/ImageList_LoadImageW, controls.ImageList_LoadImage, controls._win32_ImageList_LoadImage
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImageList_LoadImageW (Unicode) and ImageList_LoadImageA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImageList_LoadImageW
 - commctrl/ImageList_LoadImageW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
 - comdlg32.dll
api_name:
 - ImageList_LoadImage
 - ImageList_LoadImageA
 - ImageList_LoadImageW
---

# ImageList_LoadImageW function


## -description

Creates an image list from the specified bitmap.

## -parameters

### -param hi

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

A handle to the instance that contains the resource. This parameter can be <b>NULL</b> if you are loading an image from a file or loading an OEM resource.

### -param lpbmp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The image to load. 

If the <i>uFlags</i> parameter includes LR_LOADFROMFILE, <i>lpbmp</i> is the address of a null-terminated string that names the file containing the image to load.

If the <i>hi</i> parameter is non-<b>NULL</b> and LR_LOADFROMFILE is not specified, <i>lpbmp</i> is the address of a null-terminated string that contains the name of the image resource in the <i>hi</i> module.

If <i>hi</i> is <b>NULL</b> and LR_LOADFROMFILE is not specified, the <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> of this parameter must be the identifier of an OEM image to load. To create this value, use the <a href="/windows/desktop/api/winuser/nf-winuser-makeintresourcea">MAKEINTRESOURCE</a> macro with one of the OEM image identifiers defined in Winuser.h. These identifiers have the following prefixes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OBM__for_OEM_bitmaps"></a><a id="obm__for_oem_bitmaps"></a><a id="OBM__FOR_OEM_BITMAPS"></a><dl>
<dt><b>OBM_ for OEM bitmaps</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="OIC__for_OEM_icons"></a><a id="oic__for_oem_icons"></a><a id="OIC__FOR_OEM_ICONS"></a><dl>
<dt><b>OIC_ for OEM icons</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="OCR__for_OEM_cursors"></a><a id="ocr__for_oem_cursors"></a><a id="OCR__FOR_OEM_CURSORS"></a><dl>
<dt><b>OCR_ for OEM cursors</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

### -param cx

Type: <b>int</b>

The width of each image. The height of each image and the initial number of images are inferred by the dimensions of the specified resource.

### -param cGrow

Type: <b>int</b>

The number of images by which the image list can grow when the system needs to make room for new images. This parameter represents the number of new images that the resized image list can contain.

### -param crMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

The color used to generate a mask. Each pixel of this color in the specified bitmap, cursor, or icon is changed to black, and the corresponding bit in the mask is set to 1. If this parameter is the CLR_NONE value, no mask is generated. If this parameter is the CLR_DEFAULT value, the color of the pixel at the upper-left corner of the image is treated as the mask color.

### -param uType

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A flag that specifies the type of image to load. This parameter must be IMAGE_BITMAP to indicate that a bitmap is being loaded. 



<div class="alert"><b>Note</b>  <b>ImageList_LoadImage</b> is for use only with bitmap files. No other image types are supported.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_BITMAP"></a><a id="image_bitmap"></a><dl>
<dt><b>IMAGE_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
Loads a bitmap.

</td>
</tr>
</table>

### -param uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that specify how to load the image. This parameter can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LR_CREATEDIBSECTION"></a><a id="lr_createdibsection"></a><dl>
<dt><b>LR_CREATEDIBSECTION</b></dt>
</dl>
</td>
<td width="60%">
Causes the function to return a DIB section bitmap rather than a compatible bitmap when the <i>uType</i> parameter specifies IMAGE_BITMAP. LR_CREATEDIBSECTION is useful for loading a bitmap without mapping it to the colors of the display device.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTCOLOR"></a><a id="lr_defaultcolor"></a><dl>
<dt><b>LR_DEFAULTCOLOR</b></dt>
</dl>
</td>
<td width="60%">
Uses the color format of the display.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_DEFAULTSIZE"></a><a id="lr_defaultsize"></a><dl>
<dt><b>LR_DEFAULTSIZE</b></dt>
</dl>
</td>
<td width="60%">
Uses the width or height specified by the system metric values for cursors and icons if the <i>cx</i> parameter is set to zero. If this value is not specified and <i>cx</i> is set to zero, the function sets the size to the one specified in the resource. If the resource contains multiple images, the function sets the size to that of the first image. 

</td>
</tr>
<tr>
<td width="40%"><a id="LR_LOADFROMFILE"></a><a id="lr_loadfromfile"></a><dl>
<dt><b>LR_LOADFROMFILE</b></dt>
</dl>
</td>
<td width="60%">
Loads the image from the file specified by the <i>lpbmp</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_LOADMAP3DCOLORS"></a><a id="lr_loadmap3dcolors"></a><dl>
<dt><b>LR_LOADMAP3DCOLORS</b></dt>
</dl>
</td>
<td width="60%">
Searches the color table for the image and replaces the following shades of gray with the corresponding three-dimensional color: 
            
                        

Dk Gray: RGB(128, 128, 128)COLOR_3DSHADOW 



Gray: RGB(192, 192, 192)COLOR_3DFACE 



Lt Gray: RGB(223, 223, 223)COLOR_3DLIGHT 



For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_LOADTRANSPARENT"></a><a id="lr_loadtransparent"></a><dl>
<dt><b>LR_LOADTRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the color value of the first pixel in the image and replaces the corresponding entry in the color table with the default window color (the COLOR_WINDOW display color). All pixels in the image that use that color become the default window value color. This value applies only to images that have a corresponding color table. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_MONOCHROME"></a><a id="lr_monochrome"></a><dl>
<dt><b>LR_MONOCHROME</b></dt>
</dl>
</td>
<td width="60%">
Loads the image in black and white.

</td>
</tr>
<tr>
<td width="40%"><a id="LR_SHARED"></a><a id="lr_shared"></a><dl>
<dt><b>LR_SHARED</b></dt>
</dl>
</td>
<td width="60%">
Shares the image handle if the image is loaded multiple times. Do not use this value for images that have nontraditional sizes that might change after loading or for images that are loaded from a file. 

</td>
</tr>
</table>

## -returns

Type: <b>HIMAGELIST</b>

Returns the handle to the image list if successful, or <b>NULL</b> otherwise.

## -remarks

LR_LOADTRANSPARENT does not load the image transparently. It creates an opaque image list that only appears transparent because all the background pixels have been changed to COLOR_WINDOW. If the images are drawn over a background that is not the color COLOR_WINDOW, the image does not draw properly. Also, LR_LOADTRANSPARENT and LR_LOADMAP3DCOLORS use the system colors that were in effect at the time that <b>ImageList_LoadImage</b> was called. If the system colors subsequently change, the application must reload the image to remap the colors.





> [!NOTE]
> The commctrl.h header defines ImageList_LoadImage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-loadimagea">LoadImage</a>
