---
UID: NF:winddi.DrvQueryFontTree
title: DrvQueryFontTree function (winddi.h)
author: windows-sdk-content
description: The DrvQueryFontTree function provides GDI with a pointer to a structure that defines one of the following:A mapping from Unicode to glyph handles, including glyph variantsA mapping of kerning pairs to kerning handles
old-location: display\drvqueryfonttree.htm
tech.root: display
ms.assetid: 29601ea6-9b68-4cdc-a7a1-b6a922524760
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrvQueryFontTree, DrvQueryFontTree function [Display Devices], ddifncs_7f9eb5d2-dedd-4c72-8c12-0a382ea59ff4.xml, display.drvqueryfonttree, winddi/DrvQueryFontTree
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
 - winddi.h
api_name:
 - DrvQueryFontTree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DrvQueryFontTree function


## -description


The <b>DrvQueryFontTree</b> function provides GDI with a pointer to a structure that defines one of the following:
<ul>
<li>
A mapping from Unicode to glyph handles, including glyph variants

</li>
<li>
A mapping of kerning pairs to kerning handles 

</li>
</ul>

## -parameters




### -param dhpdev

Identifies a device by a handle to its <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>, returned from a prior call to <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>.


### -param iFile

Identifies the driver font file. This value is returned by <a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>.


### -param iFace

Specifies the one-based index of the driver font.


### -param iMode

Specifies the type of information to be provided. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
QFT_GLYPHSET

</td>
<td>
GDI requests a pointer to an <a href="https://msdn.microsoft.com/af56f2a0-92a6-4217-8121-944a0b4f26f6">FD_GLYPHSET</a> structure that defines the mappings from single Unicode characters to glyph handles.

</td>
</tr>
<tr>
<td>
QFT_KERNPAIRS

</td>
<td>
GDI requests a pointer to a sorted, null-terminated array of <a href="https://msdn.microsoft.com/5c5eced6-a0a3-448e-bcb3-57be1b703797">FD_KERNINGPAIR</a> structures.

The kerning pairs should be stored in increasing order. The primary key is the second Unicode character; the secondary key is the first Unicode character in the kerning pair.

</td>
</tr>
</table>
 


### -param pid

Pointer to a memory location holding the address of a driver-defined value. GDI passes the contents of *<i>pid</i> to <a href="https://msdn.microsoft.com/829e8128-f57f-433c-9c09-7e4dc0ef54be">DrvFree</a>, along with the returned pointer, when the FD_GLYPHSET structure or array of FD_KERNINGPAIR structures are no longer needed. Depending on how memory is managed in the driver, the driver-defined value can identify the structure, identify the way it was allocated, or do nothing at all.


## -returns



The return value is a pointer to the requested structure if the function is successful. Otherwise, it is <b>NULL</b>, and an error code is logged.




## -remarks



The returned structure must remain unmodified until GDI calls <a href="https://msdn.microsoft.com/829e8128-f57f-433c-9c09-7e4dc0ef54be">DrvFree</a> with the address of the structure.

<b>DrvQueryFontTree</b> is required for font drivers and drivers that use device-specific fonts.




## -see-also




<a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/829e8128-f57f-433c-9c09-7e4dc0ef54be">DrvFree</a>



<a href="https://msdn.microsoft.com/d9bcf8f8-40bc-48dc-85b7-67773c8a4ded">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/3f6efd3c-3ddf-4ce6-9527-730e01c45e74">DrvQueryFontData</a>



<a href="https://msdn.microsoft.com/29601ea6-9b68-4cdc-a7a1-b6a922524760">DrvQueryFontTree</a>



<a href="https://msdn.microsoft.com/af56f2a0-92a6-4217-8121-944a0b4f26f6">FD_GLYPHSET</a>



<a href="https://msdn.microsoft.com/5c5eced6-a0a3-448e-bcb3-57be1b703797">FD_KERNINGPAIR</a>



<a href="https://msdn.microsoft.com/fd2606ed-ec61-430a-aaad-38a4c3a207b6">IFIMETRICS</a>
 

 

