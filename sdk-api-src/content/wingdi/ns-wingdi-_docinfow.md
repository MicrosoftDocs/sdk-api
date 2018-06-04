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

# _DOCINFOW structure


## -description



The <b>DOCINFO</b> structure contains the input and output file names and other information used by the <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> function.




## -struct-fields




### -field cbSize

The size, in bytes, of the structure.


### -field lpszDocName

Pointer to a null-terminated string that specifies the name of the document.


### -field lpszOutput

Pointer to a null-terminated string that specifies the name of an output file. If this pointer is <b>NULL</b>, the output will be sent to the device identified by the device context handle that was passed to the <a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a> function.


### -field lpszDatatype

Pointer to a null-terminated string that specifies the type of data used to record the print job. The legal values for this member can be found by calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff548757">EnumPrintProcessorDatatypes</a> and can include such values as raw, emf, or XPS_PASS. This member can be <b>NULL</b>. Note that the requested data type might be ignored.


### -field fwType

Specifies additional information about the print job. This member must be zero or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DI_APPBANDING</td>
<td>Applications that use banding should set this flag for optimal performance during printing.</td>
</tr>
<tr>
<td>DI_ROPS_READ_DESTINATION</td>
<td>The application will use raster operations that involve reading from the destination surface.</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>



<a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a>
 

 

