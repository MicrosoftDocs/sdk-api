---
UID: NF:clfsw32.SetLogArchiveTail
title: SetLogArchiveTail function (clfsw32.h)
description: Sets the last archived log sequence number (LSN) or archive tail of an archivable log.
helpviewer_keywords: ["SetLogArchiveTail","SetLogArchiveTail function [Files]","clfsw32/SetLogArchiveTail","fs.setlogarchivetail"]
old-location: fs\setlogarchivetail.htm
tech.root: fs
ms.assetid: 0cdd0b85-d53e-432d-962d-9e89143ec4c7
ms.date: 12/05/2018
ms.keywords: SetLogArchiveTail, SetLogArchiveTail function [Files], clfsw32/SetLogArchiveTail, fs.setlogarchivetail
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
 - SetLogArchiveTail
 - clfsw32/SetLogArchiveTail
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
 - SetLogArchiveTail
---

# SetLogArchiveTail function


## -description

Sets the last archived log sequence number (LSN) or <i>archive tail</i> of an archivable log.

## -parameters

### -param hLog [in]

A handle to the log that is obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>.  

The log handle can refer to a dedicated or multiplexed log.

### -param plsnArchiveTail [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies a valid physical LSN in the log.


<div class="alert"><b>Note</b>  For handles to both a physical log or a log stream, <i>plsnArchiveTail</i> is a physical LSN, because it refers to a record address in the physical log.</div>
<div> </div>

### -param pReserved [in, out, optional]

This parameter is reserved and should be set to <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

The following  list identifies the possible error codes:

## -remarks

If there are any archive contexts obtained from <a href="/windows/desktop/api/clfsw32/nf-clfsw32-preparelogarchive">PrepareLogArchive</a> that are not terminated with <a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatelogarchive">TerminateLogArchive</a>, the change does not take effect until all archives are complete. While there are outstanding archive contexts, only the greatest archive tail is applied.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-removelogcontainer">RemoveLogContainer</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-removelogcontainerset">RemoveLogContainerSet</a>