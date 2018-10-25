---
UID: NS:msinkaut.tagINKMETRIC
title: tagINKMETRIC
author: windows-sdk-content
description: Specifies display properties for a text ink object (tInk).
old-location: tablet\inkmetric.htm
tech.root: tablet
ms.assetid: 27d56034-725d-4b05-9c43-6b3180d7411b
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: "*PINKMETRIC, 27d56034-725d-4b05-9c43-6b3180d7411b, IMF_BOLD, IMF_FONT_SELECTED_IN_HDC, IMF_ITALIC, INKMETRIC, INKMETRIC structure [Tablet PC], PINKMETRIC, PINKMETRIC structure pointer [Tablet PC], msinkaut/INKMETRIC, msinkaut/PINKMETRIC, tablet.inkmetric, tagINKMETRIC"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
 - msinkaut.h
api_name:
 - INKMETRIC
product: Windows
targetos: Windows
req.typenames: INKMETRIC, *PINKMETRIC
req.redist: 
---

# tagINKMETRIC structure


## -description



Specifies display properties for a text ink object (tInk).




## -struct-fields




### -field iHeight

Ink height.


### -field iFontAscent

Assent height.


### -field iFontDescent

Descent height.


### -field dwFlags

Ink metric flags.

<table>
<tr>
<th>Ink Metric Flags </th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMF_FONT_SELECTED_IN_HDC"></a><a id="imf_font_selected_in_hdc"></a><dl>
<dt><b>IMF_FONT_SELECTED_IN_HDC</b></dt>
</dl>
</td>
<td width="60%">
Use the ambient properties of the surrounding text.


</td>
</tr>
<tr>
<td width="40%"><a id="IMF_ITALIC"></a><a id="imf_italic"></a><dl>
<dt><b>IMF_ITALIC</b></dt>
</dl>
</td>
<td width="60%">
Apply the italic style.


</td>
</tr>
<tr>
<td width="40%"><a id="IMF_BOLD"></a><a id="imf_bold"></a><dl>
<dt><b>IMF_BOLD</b></dt>
</dl>
</td>
<td width="60%">
Apply the bold style.


</td>
</tr>
</table>
 


### -field color

Ink color.


## -remarks



The <b>iHeight</b>, <b>iFontAssent</b> and <b>iFontDescent</b> fields are in <b>HIMETRIC</b> units.

Applying italics to a text ink object slants the ink to the right.




## -see-also




<a href="https://msdn.microsoft.com/8f894963-7075-46f4-8809-82d1aa7e13e7">GetFormat Method</a>



<a href="https://msdn.microsoft.com/0082b7d3-61b2-478a-a6dd-ba59c20b7e1d">GetInkExtent Method</a>



<a href="https://msdn.microsoft.com/42e16e86-fc90-4089-9ae0-9a896cbeaccc">SetFormat Method</a>
 

 

