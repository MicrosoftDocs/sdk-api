---
UID: NF:olectl.OleLoadPictureFileEx
title: OleLoadPictureFileEx function (olectl.h)
description: Loads a picture from a file.
helpviewer_keywords: ["LP_COLOR","LP_DEFAULT","LP_MONOCHROME","LP_VGACOLOR","OleLoadPictureFileEx","OleLoadPictureFileEx function [Automation]","_oa96_OleLoadPictureFileEx","automat.oleloadpicturefileex","olectl/OleLoadPictureFileEx"]
old-location: automat\oleloadpicturefileex.htm
tech.root: automat
ms.assetid: 39a2c814-97f6-4157-8884-8b3f268d3f7f
ms.date: 12/05/2018
ms.keywords: LP_COLOR, LP_DEFAULT, LP_MONOCHROME, LP_VGACOLOR, OleLoadPictureFileEx, OleLoadPictureFileEx function [Automation], _oa96_OleLoadPictureFileEx, automat.oleloadpicturefileex, olectl/OleLoadPictureFileEx
req.header: olectl.h
req.include-header: 
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleLoadPictureFileEx
 - olectl/OleLoadPictureFileEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OleLoadPictureFileEx
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

