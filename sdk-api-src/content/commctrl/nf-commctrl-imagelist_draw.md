---
UID: NF:commctrl.ImageList_Draw
title: ImageList_Draw function
author: windows-driver-content
description: Draws an image list item in the specified device context.
old-location: controls\ImageList_Draw.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_draw.htm
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: ILD_BLEND, ILD_BLEND25, ILD_BLEND50, ILD_FOCUS, ILD_IMAGE, ILD_MASK, ILD_NORMAL, ILD_SELECTED, ILD_TRANSPARENT, ImageList_Draw, ImageList_Draw function [Windows Controls], _win32_ImageList_Draw, _win32_ImageList_Draw_cpp, commctrl/ImageList_Draw, controls.ImageList_Draw, controls._win32_ImageList_Draw
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
-	comdlg32.dll
api_name:
-	ImageList_Draw
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_Draw function


## -description


Draws an image list item in the specified device context. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param i

Type: <b>int</b>

The zero-based index of the image to draw. 


### -param hdcDst

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

A handle to the destination device context. 


### -param x

Type: <b>int</b>

The x-coordinate at which to draw within the specified device context. 


### -param y

Type: <b>int</b>

The y-coordinate at which to draw within the specified device context. 


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
Draws the image, blending 25 percent with the system highlight color. This value has no effect if the image list does not contain a mask.

</td>
</tr>
<tr>
<td width="40%"><a id="ILD_BLEND50"></a><a id="ild_blend50"></a><dl>
<dt><b>ILD_BLEND50</b></dt>
</dl>
</td>
<td width="60%">
Draws the image, blending 50 percent with the system highlight color. This value has no effect if the image list does not contain a mask.

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
Set this flag if the overlay does not require a mask to be drawn. This flag causes <a href="https://msdn.microsoft.com/f531f9b8-a2f5-488b-952b-f439efd83a77">ImageList_DrawEx</a> to draw just the image, ignoring the mask.

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



An overlay image is drawn transparently over the primary image specified in the <i>i</i> parameter. To specify an overlay image in the <i>fStyle</i> parameter, use the <a href="https://msdn.microsoft.com/6619d390-0c23-41ff-a07b-31425e47712b">INDEXTOOVERLAYMASK</a> macro to shift the one-based index of the overlay image. Use the OR operator to logically combine the return value of the macro with the drawing style flags specified in the <i>fStyle</i> parameter. You must first specify this image as an overlay image by using the <a href="https://msdn.microsoft.com/8cb1babc-01bd-4aae-9bc7-073050242ce4">ImageList_SetOverlayImage</a> function. 



