---
UID: NS:winbase.FILE_ID_DESCRIPTOR
title: FILE_ID_DESCRIPTOR (winbase.h)
description: Specifies the type of ID that is being used.
helpviewer_keywords: ["*LPFILE_ID_DESCRIPTOR","ExtendedFileIdType","FILE_ID_DESCRIPTOR","FILE_ID_DESCRIPTOR structure [Files]","FileIdType","ObjectIdType","fileextd/FILE_ID_DESCRIPTOR","fs.file_id_descriptor","winbase/FILE_ID_DESCRIPTOR"]
old-location: fs\file_id_descriptor.htm
tech.root: fs
ms.assetid: 9092a701-3b47-4c4c-8221-54fa3220d322
ms.date: 12/05/2018
ms.keywords: '*LPFILE_ID_DESCRIPTOR, ExtendedFileIdType, FILE_ID_DESCRIPTOR, FILE_ID_DESCRIPTOR structure [Files], FileIdType, ObjectIdType, fileextd/FILE_ID_DESCRIPTOR, fs.file_id_descriptor, winbase/FILE_ID_DESCRIPTOR'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: FILE_ID_DESCRIPTOR, *LPFILE_ID_DESCRIPTOR
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - FILE_ID_DESCRIPTOR
 - winbase/FILE_ID_DESCRIPTOR
 - LPFILE_ID_DESCRIPTOR
 - winbase/LPFILE_ID_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - FileExtd.h
api_name:
 - FILE_ID_DESCRIPTOR
---

# FILE_ID_DESCRIPTOR structure


## -description

Specifies the type of ID that is being used.

## -struct-fields

### -field dwSize

The size of this <b>FILE_ID_DESCRIPTOR</b> 
      structure.

### -field Type

The discriminator for the union indicating the type of identifier that is being passed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FileIdType"></a><a id="fileidtype"></a><a id="FILEIDTYPE"></a><dl>
<dt><b>FileIdType</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Use the <b>FileId</b> member of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="ObjectIdType"></a><a id="objectidtype"></a><a id="OBJECTIDTYPE"></a><dl>
<dt><b>ObjectIdType</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use the <b>ObjectId</b> member of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="ExtendedFileIdType"></a><a id="extendedfileidtype"></a><a id="EXTENDEDFILEIDTYPE"></a><dl>
<dt><b>ExtendedFileIdType</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Use the <b>ExtendedFileId</b> member of the union.
        

<b>Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.FileId

The ID of the file to open.

### -field DUMMYUNIONNAME.ObjectId

The ID of the object to open.

### -field DUMMYUNIONNAME.ExtendedFileId

A <a href="/windows/desktop/api/winnt/ns-winnt-file_id_128">FILE_ID_128</a> structure containing the 128-bit file ID of the file. This is used on ReFS file systems.
       

<b>Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 and Windows Server 2008 R2:  </b>This member is not supported before Windows 8 and Windows Server 2012.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-file_id_128">FILE_ID_128</a>



<a href="/windows/desktop/api/winbase/ne-winbase-file_id_type">FILE_ID_TYPE</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfilebyid">OpenFileById</a>