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

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0006 structure


## -description



The <b>SECTION</b> structure represents a short header from an MPEG-2 table section.




## -struct-fields




### -field TableId

Specifies the table identifier (TID) of the section.


### -field Header

A union that contains the following members.


### -field Header.S

Contains header bits, as an <b>MPEG_HEADER_BITS_MIDL</b> structure. Applications should use the <b>Header.W</b> field instead.


### -field Header.W

Contains the header bits as a <b>WORD</b> type. To get the individual bit fields, coerce this member to an <a href="https://msdn.microsoft.com/e25d36af-ee72-4986-8d96-2bce8b19ac80">MPEG_HEADER_BITS</a> structure.


### -field SectionData

Contains the section data, as a byte array. The length of the array is given by the <b>Header.W.SectionLength</b> field.


## -remarks



This structure represents an MPEG-2 short header. The section might contain a long header or DSM-CC header, each of which extends the short header:

<ul>
<li>If the <b>Header.W.SectionSyntaxIndicator</b> bit is set, the section uses the long syntax. In that case, you can cast a <b>SECTION</b> pointer to a <a href="https://msdn.microsoft.com/1403971f-5165-484c-9aa3-0cd489985545">LONG_SECTION</a> pointer.</li>
<li>If the TID indicates a DSM-CC user-to-network message (0x3B) or a download data message (0x3C), the section uses the DSM-CC header syntax. In that case, you can cast a <b>SECTION</b> pointer to a <a href="https://msdn.microsoft.com/b043f63c-cee0-4167-9b11-09b747f63b8d">DSMCC_SECTION</a> pointer.</li>
</ul>
The following code shows how to access the bit fields within the <b>Header</b> member:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
SECTION *pSection; // Points to the section data.

// Coerce the Header field to an MPEG_HEADER_BITS type.
MPEG_HEADER_BITS *pHeader = (MPEG_HEADER_BITS*)&amp;pSection-&gt;Header.W;

// Now use the pHeader pointer to access the bit fields.
WORD SectionLength = pHeader-&gt;SectionLength;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

