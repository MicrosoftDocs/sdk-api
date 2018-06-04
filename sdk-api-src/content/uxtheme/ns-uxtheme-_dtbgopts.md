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

# _DTBGOPTS structure


## -description


Defines the options for the <a href="https://msdn.microsoft.com/2a961479-9fdf-4f9f-923e-2a6601a99442">DrawThemeBackgroundEx</a> function.


## -struct-fields




### -field dwSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Size of the structure. Set this to sizeof(DTBGOPTS).


### -field dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Flags that specify the selected options. This member can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DTBG_CLIPRECT"></a><a id="dtbg_cliprect"></a><dl>
<dt><b>DTBG_CLIPRECT</b></dt>
</dl>
</td>
<td width="60%">
<b>rcClip</b> specifies the rectangle to which drawing is clipped.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_DRAWSOLID"></a><a id="dtbg_drawsolid"></a><dl>
<dt><b>DTBG_DRAWSOLID</b></dt>
</dl>
</td>
<td width="60%">
Deprecated. Draw transparent and alpha images as solid.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_OMITBORDER"></a><a id="dtbg_omitborder"></a><dl>
<dt><b>DTBG_OMITBORDER</b></dt>
</dl>
</td>
<td width="60%">
Do not draw the border of the part (currently this value is only supported for bgtype=borderfill).

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_OMITCONTENT"></a><a id="dtbg_omitcontent"></a><dl>
<dt><b>DTBG_OMITCONTENT</b></dt>
</dl>
</td>
<td width="60%">
Do not draw the content area of the part (currently this value is only supported for bgtype=borderfill).

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_COMPUTINGREGION"></a><a id="dtbg_computingregion"></a><dl>
<dt><b>DTBG_COMPUTINGREGION</b></dt>
</dl>
</td>
<td width="60%">
Deprecated.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_MIRRORDC"></a><a id="dtbg_mirrordc"></a><dl>
<dt><b>DTBG_MIRRORDC</b></dt>
</dl>
</td>
<td width="60%">
Assume the <b>hdc</b> is mirrored and flip images as appropriate (currently this value is only supported for bgtype=imagefile).

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_NOMIRROR"></a><a id="dtbg_nomirror"></a><dl>
<dt><b>DTBG_NOMIRROR</b></dt>
</dl>
</td>
<td width="60%">
Do not mirror the output; even in right-to-left (RTL) layout.

</td>
</tr>
<tr>
<td width="40%"><a id="DTBG_VALIDBITS"></a><a id="dtbg_validbits"></a><dl>
<dt><b>DTBG_VALIDBITS</b></dt>
</dl>
</td>
<td width="60%">
DTBG_CLIPRECT | DTBG_DRAWSOLID | DTBG_OMITBORDER | DTBG_OMITCONTENT | DTBG_COMPUTINGREGION | DTBG_MIRRORDC | DTBG_NOMIRROR.

</td>
</tr>
</table>
 


### -field rcClip

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> that specifies the bounding rectangle of the clip region.


## -see-also




<a href="https://msdn.microsoft.com/2a961479-9fdf-4f9f-923e-2a6601a99442">DrawThemeBackgroundEx</a>
 

 

