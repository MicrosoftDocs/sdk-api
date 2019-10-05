---
UID: NE:winbase._FILE_ID_TYPE
title: FILE_ID_TYPE (winbase.h)
author: windows-sdk-content
description: Discriminator for the union in the FILE_ID_DESCRIPTOR structure.
old-location: fs\file_id_type.htm
tech.root: FileIO
ms.assetid: 7e46ba94-e3cd-4d6c-962f-5d5bd55d45a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFILE_ID_TYPE, ExtendedFileIdType, FILE_ID_TYPE, FILE_ID_TYPE enumeration [Files], FileIdType, MaximumFileIdType, ObjectIdType, PFILE_ID_TYPE, PFILE_ID_TYPE enumeration pointer [Files], fileextd/ExtendedFileIdType, fileextd/FILE_ID_TYPE, fileextd/FileIdType, fileextd/MaximumFileIdType, fileextd/ObjectIdType, fileextd/PFILE_ID_TYPE, fs.file_id_type, winbase/ExtendedFileIdType, winbase/FILE_ID_TYPE, winbase/FileIdType, winbase/MaximumFileIdType, winbase/ObjectIdType, winbase/PFILE_ID_TYPE"
ms.topic: enum
f1_keywords: 
 - "winbase/FILE_ID_TYPE"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - FileExtd.h
api_name:
 - FILE_ID_TYPE
targetos: Windows
req.typenames: FILE_ID_TYPE, *PFILE_ID_TYPE
req.redist: Windows SDK on Windows Server 2003     and Windows XP.
ms.custom: 19H1
---

# FILE_ID_TYPE enumeration


## -description


Discriminator for the union in the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-file_id_descriptor">FILE_ID_DESCRIPTOR</a> structure.


## -enum-fields




### -field FileIdType

Use the <b>FileId</b> member of the union.


### -field ObjectIdType

Use the <b>ObjectId</b> member of the union.


### -field ExtendedFileIdType

Use the <b>ExtendedFileId</b> member of the union.
      

<b>Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field MaximumFileIdType

This value is used for comparison only. All valid values are less than this value.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/ns-winbase-file_id_descriptor">FILE_ID_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-enumerations">File Management Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-openfilebyid">OpenFileById</a>
 

 

