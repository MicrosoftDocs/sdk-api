---
UID: NE:strmif.tagDVD_PREFERRED_DISPLAY_MODE
title: DVD_PREFERRED_DISPLAY_MODE (strmif.h)
author: windows-sdk-content
description: Indicates the user's preferred window aspect ratio and conversion method.
old-location: dshow\dvd_preferred_display_mode.htm
tech.root: DirectShow
ms.assetid: afb235ae-ba60-491f-8b88-7fe824f00f77
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DISPLAY_16x9, DISPLAY_4x3_LETTERBOX_PREFERRED, DISPLAY_4x3_PANSCAN_PREFERRED, DISPLAY_CONTENT_DEFAULT, DVD_PREFERRED_DISPLAY_MODE, DVD_PREFERRED_DISPLAY_MODE , DVD_PREFERRED_DISPLAY_MODE enumeration [DirectShow], DVD_PREFERRED_DISPLAY_MODEEnumeration, dshow.dvd_preferred_display_mode, strmif/DISPLAY_16x9, strmif/DISPLAY_4x3_LETTERBOX_PREFERRED, strmif/DISPLAY_4x3_PANSCAN_PREFERRED, strmif/DISPLAY_CONTENT_DEFAULT, strmif/DVD_PREFERRED_DISPLAY_MODE
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_PREFERRED_DISPLAY_MODE
product: Windows
targetos: Windows
req.typenames: DVD_PREFERRED_DISPLAY_MODE
req.redist: 
ms.custom: 19H1
---

# DVD_PREFERRED_DISPLAY_MODE enumeration


## -description


<div class="alert"><b>Note</b>  Deprecated.</div><div> </div>
Indicates the user's preferred window aspect ratio and conversion method.




## -enum-fields




### -field DISPLAY_CONTENT_DEFAULT

Use the default window size and content type.
          


### -field DISPLAY_16x9

Use a 16 x 9 window.
          


### -field DISPLAY_4x3_PANSCAN_PREFERRED

Use a 4 x 3 window and convert to pan-scan, if possible.
          


### -field DISPLAY_4x3_LETTERBOX_PREFERRED

Use a 4 x 3 window and convert to letterbox, if possible.
          


## -remarks



The <b>DVD_PREFERRED_DISPLAY_MODE</b> emumeration indicates the user's preferred window aspect ratio and preferred method of conversion of 16 x 9 content to a 4 x 3 window aspect ratio. Pan-scan and letterboxing are the two conversion methods. Displaying a video at the largest possible size inside the display window without any cropping or stretching is called displaying in letterbox format. <i>Pan-scan</i> is specifically cropping a 16 x 9 video for display in a 4 x 3 window using parameters defined by the video author.

This enumerated type indicates a preference of conversion mechanisms because some content can only be displayed using one of these methods. Content that is 4 x 3 is always converted to a 16 x 9 window by using sideboxing, where black bars are added to the right and left sides of the display instead of the top and bottom of the display as in the 16 x 9 to 4 x 3 conversion using letterboxing.

The following table shows the conversion method used between the actual content type listed in the first column, and the user display preference setting, indicated by one of the other columns.

<table>
<tr>
<th>Actual content type
            </th>
<th>16 x 9
            </th>
<th>4 x 3 pan-scan
            </th>
<th>4 x 3 letterbox
            </th>
</tr>
<tr>
<td>4 x 3</td>
<td>Sideboxing</td>
<td>None</td>
<td>None</td>
</tr>
<tr>
<td>16 x 9 letterbox only</td>
<td>None</td>
<td>Letterbox</td>
<td>Letterbox</td>
</tr>
<tr>
<td>16 x 9 pan-scan only</td>
<td>None</td>
<td>Pan-scan</td>
<td>Pan-scan</td>
</tr>
<tr>
<td>16 x 9 pan-scan or letterbox</td>
<td>None</td>
<td>Pan-scan</td>
<td>Letterbox</td>
</tr>
</table>
 

The native window size used is always the user's preferred size.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/9e68b09c-534c-46d2-bda0-72f3d1d86b66">IDvdControl::VideoModePreferrence</a>
 

 

