---
UID: NF:clfsw32.PrepareLogArchive
title: PrepareLogArchive function (clfsw32.h)
description: Prepares a physical log for archival.
helpviewer_keywords: ["PrepareLogArchive","PrepareLogArchive function [Files]","clfsw32/PrepareLogArchive","fs.preparelogarchive"]
old-location: fs\preparelogarchive.htm
tech.root: fs
ms.assetid: dfdad56a-7485-4c23-852e-819980ecd5e9
ms.date: 12/05/2018
ms.keywords: PrepareLogArchive, PrepareLogArchive function [Files], clfsw32/PrepareLogArchive, fs.preparelogarchive
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
 - PrepareLogArchive
 - clfsw32/PrepareLogArchive
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
 - PrepareLogArchive
---

# PrepareLogArchive function


## -description

Prepares a physical log for archival.  The function takes a  snapshot of the current active log, builds an ordered set of log archive descriptors for the active log extents, and returns a log archive context.

 By passing this log archive context to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-getnextlogarchiveextent">GetNextLogArchiveExtent</a>, a client can iterate through the set of log archive extents to archive the log. You can also specify a range of records to archive.

## -parameters

### -param hLog [in]

A handle to the log that is  obtained by a successful call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.  

This handle can be the handle to a dedicated or multiplexed log.

### -param pszBaseLogFileName [in, out]

A pointer to a  user-allocated buffer to receive the fully qualified path of the base log.  

If the buffer is not large enough, it contains a truncated file path on exit, and the function fails with an <i>ERROR_BUFFER_OVERFLOW</i> status code. 

The  length of the file path is returned in the variable pointed to by <i>pcActualLength</i>.  The client can re-attempt  a failed call with a  name buffer that is large enough.

### -param cLen [in]

The size of the <i>pszBaseLogFileName</i> buffer, in wide characters.

### -param plsnLow [in, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the log sequence number (LSN) of the low end of the range of the  active log where the log client needs log archival information. 

If this parameter is omitted, the low end of the range defaults to the LSN of the log archive tail.

### -param plsnHigh [in, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the LSN of the high end of the range of the  active log where the log client needs log archival information. 

If this parameter is omitted, the high end of the range defaults to the next LSN to be written to the log.

### -param pcActualLength [out, optional]

A pointer to a variable that receives the actual length of the name of the base log path, in characters.  

If this value is greater than <i>cLen</i>, the function returns an ERROR_BUFFER_OVERFLOW status with a truncated path that is stored in the <i>pszBaseLogFileName</i> buffer and all other out parameters that are not set to meaningful values.

### -param poffBaseLogFileData [out]

A pointer to a variable that receives the offset  where  the metadata begins in the base log.

The contiguous extent in the base log   <i>pszBaseLogFileName</i> represents the full contents of the log metadata—that is, from <i>poffBaseLogFileData</i> to <i>pcbBaseLogFileLength</i>.

### -param pcbBaseLogFileLength [out]

A pointer to a variable  that specifies the exact length  of the base log, in bytes.

### -param plsnBase [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to receive the base log sequence number (LSN) of the active log.

### -param plsnLast [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to receive the highest valid LSN in the active log.

### -param plsnCurrentArchiveTail [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure to receive the current LSN of the archive tail of the log.

### -param ppvArchiveContext [out]

A pointer to the variable that receives a pointer to an  archive context that the system allocates.  

The archive context maintains the cursor state of the archival iterator and the log handle context.  The archival client is responsible for releasing the context by calling <a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the possible error codes:

## -remarks

You must call <a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a> to free the archive context, or memory leaks can occur.

Until you call <a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a>, containers that are being archived cannot be recycled.

You can only perform one archive operation at a time per handle that  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a> returns.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-getnextlogarchiveextent">GetNextLogArchiveExtent</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogarchivemetadata">ReadLogArchiveMetadata</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a>