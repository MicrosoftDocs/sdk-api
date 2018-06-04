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

# DrvQueryFontFile function


## -description


The <b>DrvQueryFontFile</b> function provides font file information.


## -parameters




### -param iFile

Pointer to a driver-defined value that identifies the driver font file. This pointer is returned by a prior call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>.


### -param ulMode

Specifies the type of information to be written. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
QFF_DESCRIPTION

</td>
<td>
The function provides a string that an NT-based operating system will use to describe the font file. A null-terminated Unicode string is written to the buffer pointed to by <i>pulBuffer</i>.

</td>
</tr>
<tr>
<td>
QFF_NUMFACES

</td>
<td>
The function returns the number of typefaces in the font file; the <i>cjBuf</i> and <i>pulBuf</i> parameters are ignored. Typefaces are identified by an index ranging from one through the number of typefaces.

</td>
</tr>
</table>
 


### -param cjBuf

Specifies the size, in bytes, of the return buffer.


### -param pulBuf

Pointer to the return buffer.


## -returns



If <i>ulMode</i> is QFF_NUMFACES, then the return value is the number of faces in the font file. If <i>pulBuf</i> is <b>NULL</b>, it is the number of bytes of data that would be written to <i>pulBuf</i>; otherwise, it is the number of bytes written to <i>pulBuf</i>. If an error occurs, the return value is FD_ERROR.




## -remarks



<b>DrvQueryFontFile</b> is required for font drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556247">DrvLoadFontFile</a>
 

 

