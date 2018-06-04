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

# _IMAGE_DEBUG_DIRECTORY structure


## -description


Represents the debug directory format.


## -struct-fields




### -field Characteristics

Reserved.


### -field TimeDateStamp

The ime and date the debugging information was created.


### -field MajorVersion

The major version number of the debugging information format.


### -field MinorVersion

The minor version number of the debugging information format.


### -field Type

The format of the debugging information. This member can be one of the following values. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_UNKNOWN"></a><a id="image_debug_type_unknown"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Unknown value, ignored by all tools.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_COFF"></a><a id="image_debug_type_coff"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_COFF</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
COFF debugging information (line numbers, symbol table, and string table). This type of debugging information is also pointed to by fields in the file headers.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_CODEVIEW"></a><a id="image_debug_type_codeview"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_CODEVIEW</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
CodeView debugging information. The format of the data block is described by the CodeView 4.0 specification.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_FPO"></a><a id="image_debug_type_fpo"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_FPO</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Frame pointer omission (FPO) information. This information tells the debugger how to interpret nonstandard stack frames, which use the EBP register for a purpose other than as a frame pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_MISC"></a><a id="image_debug_type_misc"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_MISC</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Miscellaneous information.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_EXCEPTION"></a><a id="image_debug_type_exception"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_EXCEPTION</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Exception information.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_FIXUP"></a><a id="image_debug_type_fixup"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_FIXUP</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Fixup information.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DEBUG_TYPE_BORLAND"></a><a id="image_debug_type_borland"></a><dl>
<dt><b>IMAGE_DEBUG_TYPE_BORLAND</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Borland debugging information.

</td>
</tr>
</table>
 


### -field SizeOfData

The size of the debugging information, in bytes. This value does not include the debug directory itself.


### -field AddressOfRawData

The address of the debugging information when the image is loaded, relative to the image base.


### -field PointerToRawData

A file pointer to the debugging information.


## -see-also




<a href="https://msdn.microsoft.com/b88c7a21-933f-450c-97e8-04cf3c5f9b11">ImageHlp Structures</a>
 

 

