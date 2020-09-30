---
UID: NS:minwinbase._OVERLAPPED_ENTRY
title: OVERLAPPED_ENTRY (minwinbase.h)
description: Contains the information returned by a call to the GetQueuedCompletionStatusEx function.
helpviewer_keywords: ["*LPOVERLAPPED_ENTRY","LPOVERLAPPED_ENTRY","LPOVERLAPPED_ENTRY structure pointer [Files]","OVERLAPPED_ENTRY","OVERLAPPED_ENTRY structure [Files]","fs.overlapped_entry","minwinbase/LPOVERLAPPED_ENTRY","minwinbase/OVERLAPPED_ENTRY","winbase/LPOVERLAPPED_ENTRY","winbase/OVERLAPPED_ENTRY"]
old-location: fs\overlapped_entry.htm
tech.root: fs
ms.assetid: 3e244e6c-0731-477a-b1d3-2601c29449ca
ms.date: 12/05/2018
ms.keywords: '*LPOVERLAPPED_ENTRY, LPOVERLAPPED_ENTRY, LPOVERLAPPED_ENTRY structure pointer [Files], OVERLAPPED_ENTRY, OVERLAPPED_ENTRY structure [Files], fs.overlapped_entry, minwinbase/LPOVERLAPPED_ENTRY, minwinbase/OVERLAPPED_ENTRY, winbase/LPOVERLAPPED_ENTRY, winbase/OVERLAPPED_ENTRY'
req.header: minwinbase.h
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
req.typenames: OVERLAPPED_ENTRY, *LPOVERLAPPED_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OVERLAPPED_ENTRY
 - minwinbase/_OVERLAPPED_ENTRY
 - LPOVERLAPPED_ENTRY
 - minwinbase/LPOVERLAPPED_ENTRY
 - OVERLAPPED_ENTRY
 - minwinbase/OVERLAPPED_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MinWinBase.h
 - WinBase.h
api_name:
 - OVERLAPPED_ENTRY
---

# OVERLAPPED_ENTRY structure


## -description

Contains the information returned by a call to the 
    <a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a> 
    function.

## -struct-fields

### -field lpCompletionKey

Receives the completion key value associated with the file handle whose I/O operation has completed. A 
      completion key is a per-file key that is specified in a call to 
      <a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>.

### -field lpOverlapped

Receives the address of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure 
      that was specified when the completed I/O operation was started.

### -field Internal

Reserved.

### -field dwNumberOfBytesTransferred

Receives the number of bytes transferred during the I/O operation that has completed.

## -see-also

<a href="/windows/desktop/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>