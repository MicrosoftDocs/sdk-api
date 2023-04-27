---
UID: NS:minwinbase._OVERLAPPED
title: OVERLAPPED (minwinbase.h)
description: Contains information used in asynchronous (or overlapped) input and output (I/O).
helpviewer_keywords: ["*LPOVERLAPPED","LPOVERLAPPED","LPOVERLAPPED structure pointer","OVERLAPPED","OVERLAPPED structure","_win32_overlapped_str","base.overlapped_str","minwinbase/LPOVERLAPPED","minwinbase/OVERLAPPED","winbase/LPOVERLAPPED","winbase/OVERLAPPED"]
old-location: base\overlapped_str.htm
tech.root: backup
ms.assetid: 5037f6b9-e316-483b-a8e2-b58d2587ebd9
ms.date: 12/05/2018
ms.keywords: '*LPOVERLAPPED, LPOVERLAPPED, LPOVERLAPPED structure pointer, OVERLAPPED, OVERLAPPED structure, _win32_overlapped_str, base.overlapped_str, minwinbase/LPOVERLAPPED, minwinbase/OVERLAPPED, winbase/LPOVERLAPPED, winbase/OVERLAPPED'
req.header: minwinbase.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.typenames: OVERLAPPED, *LPOVERLAPPED
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OVERLAPPED
 - minwinbase/_OVERLAPPED
 - LPOVERLAPPED
 - minwinbase/LPOVERLAPPED
 - OVERLAPPED
 - minwinbase/OVERLAPPED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - minWinBase.h
api_name:
 - OVERLAPPED
---

# OVERLAPPED structure


## -description

Contains information used in asynchronous (or <i>overlapped</i>) input and output (I/O).

## -struct-fields

### -field Internal

The status code for the I/O request. When the request is issued, the system sets this member to <b>STATUS_PENDING</b> to indicate that the operation has not yet started.  When the request is completed, the system sets this member to the status code for the completed request. 

The <b>Internal</b> member was originally reserved for system use and its behavior may change.

### -field InternalHigh

The number of bytes transferred for the I/O request. The system sets this member if the request is completed without errors. 

The <b>InternalHigh</b> member was originally reserved for system use and its behavior may change.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Offset

The low-order portion of the file position at which to start the I/O request, as specified by the user. 

This member is nonzero only when performing I/O requests on a seeking device that supports the concept of an offset (also referred to as a file pointer mechanism), such as a file. Otherwise, this member must be zero.

For additional information, see Remarks.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.OffsetHigh

The high-order portion of the file position at which to start the I/O request, as specified by the user. 

This member is nonzero only when performing I/O requests on a seeking device that supports the concept of an offset (also referred to as a file pointer mechanism), such as a file. Otherwise, this member must be zero.

For additional information, see Remarks.

### -field DUMMYUNIONNAME.Pointer

Reserved for system use; do not use after initialization to zero.

### -field hEvent

A handle to the event that will be set to a signaled state by the system when the operation has completed. The user must initialize this member either to zero or a valid event handle using the <a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function before passing this structure to any overlapped functions. This event can then be used to synchronize simultaneous I/O requests for a device. For additional information, see Remarks.

Functions such as <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> and <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> set this handle to the nonsignaled state before they begin an I/O operation. When the operation has completed, the handle is set to the signaled state.

 


Functions such as <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> and the synchronization <a href="/windows/desktop/Sync/wait-functions">wait functions</a> reset auto-reset events to the nonsignaled state. Therefore, you should use a manual reset event; if you use an auto-reset event, your application can stop responding if you wait for the operation to complete and then call <b>GetOverlappedResult</b> with the <i>bWait</i> parameter set to <b>TRUE</b>.

## -remarks

Any unused members of this structure should always be initialized to zero before the structure is used in a function call.  Otherwise, the function may fail and return <b>ERROR_INVALID_PARAMETER</b>.

The <b>Offset</b> and <b>OffsetHigh</b> members together represent a 64-bit file position. It is a byte offset from the start of the file or file-like device, and it is specified by the user; the system will not modify these values. The calling process must set this member before passing the <b>OVERLAPPED</b> structure to functions that use an offset, such as the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a> or 
<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> (and related) functions.  

You can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a> macro to check whether an asynchronous I/O operation has completed if <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> is too cumbersome for your application. 

You can use the 
<a href="/windows/desktop/FileIO/cancelio">CancelIo</a> function to cancel an asynchronous I/O operation.

A common mistake is to reuse an <b>OVERLAPPED</b> structure before the previous asynchronous operation has been completed. You should use a separate structure for each request. You should also create an event object for each thread that processes data. If you store the event handles in an array, you could easily wait for all events to be signaled using the <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects">WaitForMultipleObjects</a> function.

For additional information and potential pitfalls of asynchronous I/O usage, see  <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>, <a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>, <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>, and related functions.

For a general synchronization overview and conceptual <b>OVERLAPPED</b> usage information, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a> and related topics.

For a file I/O–oriented overview of synchronous and asynchronous I/O, see <a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>.


#### Examples

For an example, see <a href="/windows/desktop/ipc/named-pipe-server-using-overlapped-i-o">Named Pipe Server Using Overlapped I/O</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/FileIO/cancelio">CancelIo</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>



<a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>