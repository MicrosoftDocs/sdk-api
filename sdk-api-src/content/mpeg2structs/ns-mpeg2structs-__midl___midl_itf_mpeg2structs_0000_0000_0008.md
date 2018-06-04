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

# __MIDL___MIDL_itf_mpeg2structs_0000_0000_0008 structure


## -description



The <b>LONG_SECTION</b> structure represents a long MPEG-2 section header. If a section contains a long header, you can cast a <a href="https://msdn.microsoft.com/6ee07b84-ae97-413f-a3b4-0078ad740194">SECTION</a> pointer to a <b>LONG_SECTION</b> pointer. For more information, see the Remarks section in the <b>SECTION</b> reference.




## -struct-fields




### -field TableId

Specifies the table identifier (TID) of the section.


### -field Header

A union that contains the following members.


### -field Header.S

Contains packed header bits, as an <b>MPEG_HEADER_BITS_MIDL</b> structure. Applications should use the <b>Header.W</b> field instead.


### -field Header.W

Contains the header bits as a <b>WORD</b> type. To get the individual bitfields, coerce this member to an <a href="https://msdn.microsoft.com/e25d36af-ee72-4986-8d96-2bce8b19ac80">MPEG_HEADER_BITS</a> structure.


### -field TableIdExtension

Specifies the table_id_extension field.


### -field Version

A union that contains the following members.


### -field Version.S

Contains the version number and current/next indicator bit as an <b>MPEG_HEADER_VERSION_BITS_MIDL</b> structure. Applications should use the <b>Version.B</b> field instead.


### -field Version.B

Contains the version number and current/next indicator bit as a <b>BYTE</b> type. To get the individual bit fields, coerce this member to an <a href="https://msdn.microsoft.com/d9a33ca6-2e35-4f7c-8621-ce30effeb687">MPEG_HEADER_VERSION_BITS</a> structure.


### -field SectionNumber

Specifies the section_number field, which gives the section number for this section.


### -field LastSectionNumber

Specifies the last_section_number field, which gives the last (highest) section number for the table.


### -field RemainingData

Contains the remaining section data, as a byte array. The length of the array is <code>Header.W.SectionLength - 5</code> bytes.


## -remarks



The following code shows how to access the bit fields within the <b>Version</b> member:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LONG_SECTION *pSection; // Points to the section data.

// Coerce the Version field to an MPEG_HEADER_VERSION_BITS type.
MPEG_HEADER_VERSION_BITS *pVersion;
pVersion = (MPEG_HEADER_VERSION_BITS*)&amp;pSection-&gt;Version.B;

// Now use the pHeader pointer to access the bit fields.
BYTE VersionNumber = pSection-&gt;VersionNumber;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5ae43ac6-519d-486b-aaa5-c766f3194ef2">BDA Structures</a>
 

 

