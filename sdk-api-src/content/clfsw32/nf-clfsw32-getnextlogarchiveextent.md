---
UID: NF:clfsw32.GetNextLogArchiveExtent
title: GetNextLogArchiveExtent function (clfsw32.h)
description: Retrieves the next set of archive extents in a log archive context.
helpviewer_keywords: ["GetNextLogArchiveExtent","GetNextLogArchiveExtent function [Files]","clfsw32/GetNextLogArchiveExtent","fs.getnextlogarchiveextent"]
old-location: fs\getnextlogarchiveextent.htm
tech.root: fs
ms.assetid: 4aaf10bd-e9df-435b-a756-5ae5c1eb2903
ms.date: 12/05/2018
ms.keywords: GetNextLogArchiveExtent, GetNextLogArchiveExtent function [Files], clfsw32/GetNextLogArchiveExtent, fs.getnextlogarchiveextent
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
 - GetNextLogArchiveExtent
 - clfsw32/GetNextLogArchiveExtent
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
 - GetNextLogArchiveExtent
---

# GetNextLogArchiveExtent function


## -description

Retrieves the next set of archive extents in a log archive context.  The log archive context describes a   contiguous set of file extents that span the snapshot of the active log  captured by  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a> captures.  <b>GetNextLogArchiveExtent</b> maintains a cursor in the ordered set of log archive descriptors so that  subsequent calls allow an application to iterate through the entire set.

## -parameters

### -param pvArchiveContext [in]

A pointer to an  archive context that is obtained by a call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a>.

  The context maintains  the cursor state, which allows iteration through the set of file extents in the archive.  The archive client is responsible for deallocating the context by using the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a> function.

### -param rgadExtent [in, out]

A client-allocated array of <a href="/windows/desktop/api/clfs/ns-clfs-cls_archive_descriptor">CLFS_ARCHIVE_DESCRIPTOR</a>  structures to be filled in by this function.

### -param cDescriptors [in]

The number of elements in  the <i>rgadExtent</i> array. 

This value is the maximum number of archive descriptors that can be retrieved by this function.

### -param pcDescriptorsReturned [out]

The number of descriptors in the <i>rgadExtent</i> array that are  filled in by this function.  

If this value is less than <i>cDescriptors</i>,  the set of descriptors is exhausted and the archive client can terminate iteration through the ordered descriptor set.  Further calls to this function fail with ERROR_NO_MORE_ENTRIES.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_archive_descriptor">CLFS_ARCHIVE_DESCRIPTOR</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>