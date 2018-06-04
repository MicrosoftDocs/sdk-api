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

# ISectionList::GetSectionData


## -description



The <b>GetSectionData</b> method retrieves a section.




## -parameters




### -param sectionNumber [in]

Specifies the section number to retrieve, indexed from zero. Call the <b>GetNumberOfSections</b> method to get the number of sections.


### -param pdwRawPacketLength [out]

Receives the size of the section data, in bytes.


### -param ppSection [out]

Address of a variable that receives a pointer to a <b>SECTION</b> structure, containing the section data. Do not free the memory for the structure; the object frees the memory when the interface is released.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The request has not completed yet.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The section number is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The section header is converted from network byte order to native byte order. The number of header bytes that are converted depends on the header type. The header types are <i>short header</i> (<a href="https://msdn.microsoft.com/6ee07b84-ae97-413f-a3b4-0078ad740194">SECTION</a> structure), <i>long header</i> (<a href="https://msdn.microsoft.com/1403971f-5165-484c-9aa3-0cd489985545">LONG_SECTION</a> structure), or <i>DSM-CC header</i> (<a href="https://msdn.microsoft.com/b043f63c-cee0-4167-9b11-09b747f63b8d">DSMCC_SECTION</a> structure). If the section has a short header, the first three bytes are converted; for a long header, the first eight bytes are converted; and for a DSM-CC header, the first 20 bytes are converted.

The body of the section data, after the header, is left unparsed and unconverted.




## -see-also




<a href="https://msdn.microsoft.com/eb6d31b4-ee4a-468f-9e58-115159095858">ISectionList Interface</a>
 

 

