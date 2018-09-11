---
UID: NS:wingdi._DOCINFOW
title: "_DOCINFOW"
author: windows-sdk-content
description: The DOCINFO structure contains the input and output file names and other information used by the StartDoc function.
old-location: gdi\docinfo.htm
tech.root: printdocs
ms.assetid: 329bf0d9-399b-4f64-a029-361ef7558aeb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDOCINFOW, DOCINFO, DOCINFO structure [Windows GDI], DOCINFOW, LPDOCINFO, LPDOCINFO structure pointer [Windows GDI], _DOCINFOW, _win32_DOCINFO_str, gdi.docinfo, wingdi/DOCINFO, wingdi/LPDOCINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Wingdi.h
api_name:
 - DOCINFO
product: Windows
targetos: Windows
req.typenames: DOCINFOW, *LPDOCINFOW
req.redist: 
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

Pointer to a null-terminated string that specifies the type of data used to record the print job. The legal values for this member can be found by calling <a href="https://msdn.microsoft.com/27b6e074-d303-446b-9e5f-6cfa55c30d26">EnumPrintProcessorDatatypes</a> and can include such values as raw, emf, or XPS_PASS. This member can be <b>NULL</b>. Note that the requested data type might be ignored.


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



<a href="https://msdn.microsoft.com/e5c115b0-9c1e-46e7-8fb5-eddbc2c75298">Printing</a>



<a href="https://msdn.microsoft.com/53143463-b9fc-4378-aea9-da6c73a7cd03">StartDoc</a>
 

 

