---
UID: NS:winnt._IMAGE_DEBUG_DIRECTORY
title: IMAGE_DEBUG_DIRECTORY (winnt.h)
description: Represents the debug directory format.
helpviewer_keywords: ["*PIMAGE_DEBUG_DIRECTORY","IMAGE_DEBUG_DIRECTORY","IMAGE_DEBUG_DIRECTORY structure","IMAGE_DEBUG_TYPE_BORLAND","IMAGE_DEBUG_TYPE_CODEVIEW","IMAGE_DEBUG_TYPE_COFF","IMAGE_DEBUG_TYPE_EXCEPTION","IMAGE_DEBUG_TYPE_FIXUP","IMAGE_DEBUG_TYPE_FPO","IMAGE_DEBUG_TYPE_MISC","IMAGE_DEBUG_TYPE_UNKNOWN","PIMAGE_DEBUG_DIRECTORY","PIMAGE_DEBUG_DIRECTORY structure pointer","_IMAGE_DEBUG_DIRECTORY","_win32_image_debug_directory_str","base.image_debug_directory_str","winnt/IMAGE_DEBUG_DIRECTORY","winnt/PIMAGE_DEBUG_DIRECTORY"]
old-location: base\image_debug_directory_str.htm
tech.root: Debug
ms.assetid: f89a3c9b-4d73-4ff5-8f45-2e58500d5084
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_DEBUG_DIRECTORY, IMAGE_DEBUG_DIRECTORY, IMAGE_DEBUG_DIRECTORY structure, IMAGE_DEBUG_TYPE_BORLAND, IMAGE_DEBUG_TYPE_CODEVIEW, IMAGE_DEBUG_TYPE_COFF, IMAGE_DEBUG_TYPE_EXCEPTION, IMAGE_DEBUG_TYPE_FIXUP, IMAGE_DEBUG_TYPE_FPO, IMAGE_DEBUG_TYPE_MISC, IMAGE_DEBUG_TYPE_UNKNOWN, PIMAGE_DEBUG_DIRECTORY, PIMAGE_DEBUG_DIRECTORY structure pointer, _IMAGE_DEBUG_DIRECTORY, _win32_image_debug_directory_str, base.image_debug_directory_str, winnt/IMAGE_DEBUG_DIRECTORY, winnt/PIMAGE_DEBUG_DIRECTORY'
f1_keywords:
- winnt/IMAGE_DEBUG_DIRECTORY
dev_langs:
- c++
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- WinNT.h
api_name:
- IMAGE_DEBUG_DIRECTORY
targetos: Windows
req.typenames: IMAGE_DEBUG_DIRECTORY, *PIMAGE_DEBUG_DIRECTORY
req.redist: 
ms.custom: 19H1
---

# IMAGE_DEBUG_DIRECTORY structure


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




<a href="https://docs.microsoft.com/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>
 

 

