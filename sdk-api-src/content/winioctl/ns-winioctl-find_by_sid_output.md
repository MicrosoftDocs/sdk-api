---
UID: NS:winioctl.__unnamed_struct_13
title: FIND_BY_SID_OUTPUT
description: Represents a file name.
helpviewer_keywords: ["*PFIND_BY_SID_OUTPUT","FIND_BY_SID_OUTPUT","FIND_BY_SID_OUTPUT structure [Files]","PFIND_BY_SID_OUTPUT","PFIND_BY_SID_OUTPUT structure pointer [Files]","base.find_by_sid_output","fs.find_by_sid_output","winioctl/FIND_BY_SID_OUTPUT","winioctl/PFIND_BY_SID_OUTPUT"]
old-location: fs\find_by_sid_output.htm
tech.root: FileIO
ms.assetid: fc616f88-c8c9-43de-8b17-2b8c38e5cdbb
ms.date: 12/05/2018
ms.keywords: '*PFIND_BY_SID_OUTPUT, FIND_BY_SID_OUTPUT, FIND_BY_SID_OUTPUT structure [Files], PFIND_BY_SID_OUTPUT, PFIND_BY_SID_OUTPUT structure pointer [Files], base.find_by_sid_output, fs.find_by_sid_output, winioctl/FIND_BY_SID_OUTPUT, winioctl/PFIND_BY_SID_OUTPUT'
f1_keywords:
- winioctl/FIND_BY_SID_OUTPUT
dev_langs:
- c++
req.header: winioctl.h
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
- WinIoCtl.h
api_name:
- FIND_BY_SID_OUTPUT
targetos: Windows
req.typenames: FIND_BY_SID_OUTPUT, *PFIND_BY_SID_OUTPUT
req.redist: 
---

# FIND_BY_SID_OUTPUT structure


## -description


Represents a file name.


## -struct-fields




### -field NextEntryOffset

 


### -field FileIndex

 


### -field FileNameLength

The size of the file name, in bytes. This size does not include the NULL character.


### -field FileName

A pointer to a null-terminated string that specifies the file name.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ni-winioctl-fsctl_find_files_by_sid">FSCTL_FIND_FILES_BY_SID</a>
 

 

