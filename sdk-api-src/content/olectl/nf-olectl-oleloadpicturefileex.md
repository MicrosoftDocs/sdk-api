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

# OleLoadPictureFileEx function


## -description


Loads a picture from a file.


## -parameters




### -param varFileName [in]

The path and name of the picture file to load.


### -param xSizeDesired [in]

The desired length for the picture to be displayed.


### -param ySizeDesired [in]

The desired height for the picture to be displayed.


### -param dwFlags [in]

The desired color depth for the icon or cursor. Together with the desired size it is used to select the best matching image.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LP_MONOCHROME_"></a><a id="lp_monochrome_"></a><dl>
<dt><b>LP_MONOCHROME
</b></dt>
</dl>
</td>
<td width="60%">
Creates a monochrome picture to display on a monitor.

</td>
</tr>
<tr>
<td width="40%"><a id="LP_VGACOLOR_"></a><a id="lp_vgacolor_"></a><dl>
<dt><b>LP_VGACOLOR
</b></dt>
</dl>
</td>
<td width="60%">
Creates a 16-color picture to display on a monitor.

</td>
</tr>
<tr>
<td width="40%"><a id="LP_COLOR_"></a><a id="lp_color_"></a><dl>
<dt><b>LP_COLOR
</b></dt>
</dl>
</td>
<td width="60%">
Creates a 256-color picture to display on a monitor.

</td>
</tr>
<tr>
<td width="40%"><a id="LP_DEFAULT_"></a><a id="lp_default_"></a><dl>
<dt><b>LP_DEFAULT
</b></dt>
</dl>
</td>
<td width="60%">
Selects the best color depth to use for the current display.

</td>
</tr>
</table>
 


### -param lplpdispPicture [out]

The location that receives a pointer to the picture.


## -returns



This method returns standard COM error codes in addition to the following values.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_PARAMNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
<i>varFileName</i> is not valid.

</td>
</tr>
</table>
 




## -remarks



Recognized graphic formats include bitmap (.bmp), JPEG (.jpg), GIF (.gif), and PGN (.png) files.



