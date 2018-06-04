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

# DrvQueryAdvanceWidths function


## -description


The <b>DrvQueryAdvanceWidths</b> function returns character advance widths for a specified set of glyphs.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> that was previously returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param pfo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> structure that identifies the font instance.


### -param iMode

Specifies the type of information to be provided. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
QAW_GETEASYWIDTHS

</td>
<td>
The character advance widths are returned as an array of 12.4 fixed-point numbers. This mode will not be used if the widths exceed the range of the 12.4 representation. This routine should compute widths as quickly as possible. If the computation of a glyph's character advance width cannot be accomplished efficiently, the driver should write 0xFFFF into the buffer for that glyph. The function returns DDI_ERROR if an error occurs, <b>FALSE</b> if not all widths can be efficiently computed for this mode, or <b>TRUE</b> in all other cases.

</td>
</tr>
<tr>
<td>
QAW_GETWIDTHS

</td>
<td>
The character advance widths are recorded as an array of 12.4 fixed-point numbers. This mode will not be used if the widths exceed the range of the 12.4 representation. The function returns <b>TRUE</b> if successful.

</td>
</tr>
</table>
 


### -param phg [in]

Pointer to an array of glyph handles that specify the glyphs for which the driver will return character advance widths.


### -param pvWidths [out]

Pointer to a buffer where the driver will record data.


### -param cGlyphs

Specifies the number of glyphs in the input buffer pointed to by <i>phg</i>.


## -returns



The return value is dependent on the value of the <i>iMode</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

