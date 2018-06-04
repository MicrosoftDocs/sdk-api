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

Identifies a device by a handle to its <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>, returned from a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param iFile

Identifies the driver font file. This value is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>.


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
GDI requests a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff565625">FD_GLYPHSET</a> structure that defines the mappings from single Unicode characters to glyph handles.

</td>
</tr>
<tr>
<td>
QFT_KERNPAIRS

</td>
<td>
GDI requests a pointer to a sorted, null-terminated array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff565630">FD_KERNINGPAIR</a> structures.

The kerning pairs should be stored in increasing order. The primary key is the second Unicode character; the secondary key is the first Unicode character in the kerning pair.

</td>
</tr>
</table>
 


### -param pid

Pointer to a memory location holding the address of a driver-defined value. GDI passes the contents of *<i>pid</i> to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556226">DrvFree</a>, along with the returned pointer, when the FD_GLYPHSET structure or array of FD_KERNINGPAIR structures are no longer needed. Depending on how memory is managed in the driver, the driver-defined value can identify the structure, identify the way it was allocated, or do nothing at all.


## -returns



The return value is a pointer to the requested structure if the function is successful. Otherwise, it is <b>NULL</b>, and an error code is logged.




## -remarks



The returned structure must remain unmodified until GDI calls <a href="https://msdn.microsoft.com/library/windows/hardware/ff556226">DrvFree</a> with the address of the structure.

<b>DrvQueryFontTree</b> is required for font drivers and drivers that use device-specific fonts.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552835">DEVINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556226">DrvFree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556264">DrvQueryFontData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556266">DrvQueryFontTree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565625">FD_GLYPHSET</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565630">FD_KERNINGPAIR</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567418">IFIMETRICS</a>
 

 

