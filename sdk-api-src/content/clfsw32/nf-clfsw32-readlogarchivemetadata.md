---
UID: NF:clfsw32.ReadLogArchiveMetadata
title: ReadLogArchiveMetadata function (clfsw32.h)
description: Copies a range of the archive view of the metadata to the specified buffer.
helpviewer_keywords: ["ReadLogArchiveMetadata","ReadLogArchiveMetadata function [Files]","clfsw32/ReadLogArchiveMetadata","fs.readlogarchivemetadata"]
old-location: fs\readlogarchivemetadata.htm
tech.root: fs
ms.assetid: b0b8528d-30fc-4995-b82d-5577af8d299d
ms.date: 12/05/2018
ms.keywords: ReadLogArchiveMetadata, ReadLogArchiveMetadata function [Files], clfsw32/ReadLogArchiveMetadata, fs.readlogarchivemetadata
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReadLogArchiveMetadata
 - clfsw32/ReadLogArchiveMetadata
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - ReadLogArchiveMetadata
---

# ReadLogArchiveMetadata function


## -description

Copies a range of the archive view of the metadata to the specified buffer.

## -parameters

### -param pvArchiveContext [in]

A pointer to an  archive context that is obtained by a call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a>.

  The context maintains  the cursor state, which allows iteration through the set of file extents in the archive.  The archive client is responsible for deallocating the context by using the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a> function.

### -param cbOffset [in]

The offset in the metadata where data copying starts.  

On the first call to this function, specify zero (0). On subsequent calls, specify the value that is returned in <i>pcbBytesRead</i>.

### -param cbBytesToRead [in]

The number of bytes of the metadata snapshot should be copied into <i>pbReadBuffer</i>.  

This parameter cannot be zero (0).

### -param pbReadBuffer [in, out]

A pointer to the buffer  where the metadata snapshot is copied.

### -param pcbBytesRead [out]

A pointer to a variable that receives the number of bytes  that are  copied to <i>pbReadBuffer</i>.  

The number of bytes is always between zero (0) and <i>cbBytesToRead</i>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies  the possible error codes:

## -see-also

<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a>