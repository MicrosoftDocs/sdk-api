---
UID: NF:cimfs.CimWriteStream
title: CimWriteStream
description: The CimWriteStream function writes data from the specified buffer to the stream represented by the stream handle.
ms.date: 08/01/2022
tech.root: cimfs
ms.keywords: CimWriteStream
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: cimfs.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: cimfs.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - cimfs.h
api_name:
 - CimWriteStream
f1_keywords:
 - CimWriteStream
 - cimfs/CimWriteStream
---

## -description

Writes data from the specified buffer to the stream represented by the stream handle.

## -parameters

### -param cimStreamHandle

Type: **CIMFS_STREAM_HANDLE**
An opaque handle that represents a writer for the stream created with CimCreateFile or CimCreateAlternateStream.

### -param buffer

TYPE: **void\***
A caller allocated buffer that contains the data to be written

### -param bufferSize

Type **[UINT32](/windows/desktop/winprog/windows-data-types)**
The size of the caller allocated buffer. The contents of the buffer will be written to the stream up to but not exceeding the stream size provided when the stream was created.

## -returns

**[HRESULT](/windows/desktop/winprog/windows-data-types)**
E_INVALIDARG – The stream handle is invalid or the handle provided refers to a directory rather than a file or alternate stream.
E_POINTER – The buffer pointer is NULL
HRESULT_FROM_WIN32(ERROR_HANDLE_EOF) – The write extends past the file size specified when the stream was created. The data written was truncated at the end of file.

## -remarks

## -see-also
