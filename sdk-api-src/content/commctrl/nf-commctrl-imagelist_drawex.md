---
UID: NF:commctrl.ImageList_DrawEx
title: ImageList_DrawEx function
author: windows-sdk-content
description: Draws an image list item in the specified device context. The function uses the specified drawing style and blends the image with the specified color.
old-location: controls\ImageList_DrawEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_drawex.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CLR_DEFAULT, CLR_NONE, ILD_BLEND, ILD_BLEND25, ILD_BLEND50, ILD_FOCUS, ILD_IMAGE, ILD_MASK, ILD_NORMAL, ILD_SELECTED, ILD_TRANSPARENT, ImageList_DrawEx, ImageList_DrawEx function [Windows Controls], _win32_ImageList_DrawEx, _win32_ImageList_DrawEx_cpp, commctrl/ImageList_DrawEx, controls.ImageList_DrawEx, controls._win32_ImageList_DrawEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ImageList_DrawEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_DrawEx function


## -description


Draws an image list item in the specified device context. The function uses the specified drawing style and blends the image with the specified color. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list 


### -param i

Type: <b>int</b>

The index of the image to draw. 


### -param hdcDst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

A handle to the destination device context. 


### -param x

Type: <b>int</b>

The x-coordinate at which to draw within the specified device context. 


### -param y

Type: <b>int</b>

The y-coordinate at which to draw within the specified device context. 


### -param dx

Type: <b>int</b>

The width of the portion of the image to draw relative to the upper-left corner of the image. If <i>dx</i> and 
<i>dy</i> are zero, the function draws the entire image. The function does not ensure that the parameters are valid. 


### -param dy

Type: <b>int</b>

The height of the portion of the image to draw, relative to the upper-left corner of the image. If 
					<i>dx</i> and 
					<i>dy</i> are zero, the function draws the entire image. The function does not ensure that the parameters are valid. 


### -param rgbBk

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The background color of the image. This parameter can be an application-defined RGB value or one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLR_NONE"></a><a id="clr_none"></a><dl>
<dt><b>CLR_NONE</b></dt>
</dl>
</td>
<td width="60%">
No background color. The image is drawn transparently.

</td>
</tr>
<tr>
<td width="40%"><a id="CLR_DEFAULT"></a><a id="clr_default"></a><dl>
<dt><b>CLR_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The default background color. The image is drawn using the background color of the image list.

</td>
</tr>
</table>
 


### -param rgbFg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The foreground color of the image. This parameter can be an application-defined RGB value or one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLR_NONE"></a><a id="clr_none"></a><dl>
<dt><b>CLR_NONE</b></dt>
</dl>
</td>
<td width="60%">
No blend color. The image is blended with the color of the destination device context.

</td>
</tr>
<tr>
<td width="40%"><a id="CLR_DEFAULT"></a><a id="clr_default"></a><dl>
<dt><b>CLR_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The default foreground color. The image is drawn using the system highlight color as the foreground color. 

</td>
</tr>
</table>
 


### -param fStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The drawing style and, optionally, the overlay image. For information about specifying an overlay image index, see the comments section at the end of this topic. This parameter can be a combination of an overlay image index and one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ILD_BLEND"></a><a id="ild_blend"></a><dl>
<dt><b>ILD_BLEND</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="ILD_BLEND25"></a><a id="ild_blend25"></a><dl>
<dt><b>ILD_BLEND25</b></dt>
</dl>
</td>
<td width="60%">
Draws the image, blending 25 percent with the blend color specified by <i>rgbFg</i>. This value has no effect if the image list does not contain a mask.

</td>
</tr>
<tr>
<td width="40%"><a id="ILD_BLEND50"></a><a id="ild_blend50"></a><dl>
<dt><b>ILD_BLEND50</b></dt>
</dl>
</td>
<td width="60%">
Draws the image, blending 50 percent with the blend color specified by <i>rgbFg</i>. This value has no effect if the image list does not contain a mask.

</td>
</tr>
<tr>
<td width="40%"><a id="ILD_FOCUS"></a><a id="ild_focus"></a><dl>
<dt><b>ILD_FOCUS</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="ILD_IMAGE"></a><a id="ild_image"></a><dl>
<dt><b>ILD_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
Set this flag if the overlay does not require a mask to be drawn. This flag causes <b>ImageList_DrawEx</b> to draw just the image, ignoring the mask.

</td>
</tr>
<tr>
<td width="40%"><a id="ILD_MASK"></a><a id="ild_mask"></a><dl>
<dt><b>ILD_MASK</b></dt>
</dl>
</td>
<td width="60%">
Draws the mask.

</td>
</tr>
<tr>
<td width="40%"><a id="ILD_NORMAL"></a><a id="ild_normal"></a><dl>
<dt><b>ILD_NORMAL</b></dt>
</dl>
</td>
<td width="60%">
Draws the image using the background color for the image list. If the background color is the CLR_NONE value, the image is drawn transparently using the mask.

</td>
</tr>
<tr>
<td width="40%"><a id="ILD_SELECTED"></a><a id="ild_selected"></a><dl>
<dt><b>ILD_SELECTED</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="ILD_TRANSPARENT"></a><a id="ild_transparent"></a><dl>
<dt><b>ILD_TRANSPARENT</b></dt>
</dl>
</td>
<td width="60%">
Draws the image transparently using the mask, regardless of the background color. This value has no effect if the image list does not contain a mask.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



An overlay image is drawn transparently over the primary image specified in the <i>i</i> parameter. To specify an overlay image in the <i>fStyle</i> parameter, use the <a href="https://msdn.microsoft.com/en-us/library/Bb761408(v=VS.85).aspx">INDEXTOOVERLAYMASK</a> macro to shift the one-based index of the overlay image. Use the OR operator to logically combine the return value of the macro with the drawing style flags specified in the <i>fStyle</i> parameter. You must first specify this image as an overlay image by using the <a href="https://msdn.microsoft.com/en-us/library/Bb775227(v=VS.85).aspx">ImageList_SetOverlayImage</a> function. 



