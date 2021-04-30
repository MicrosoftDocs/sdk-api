---
UID: NF:winbase.SetFileCompletionNotificationModes
title: SetFileCompletionNotificationModes function (winbase.h)
description: Sets the notification modes for a file handle, allowing you to specify how completion notifications work for the specified file.
helpviewer_keywords: ["FILE_SKIP_COMPLETION_PORT_ON_SUCCESS","FILE_SKIP_SET_EVENT_ON_HANDLE","SetFileCompletionNotificationModes","SetFileCompletionNotificationModes function [Files]","fs.setfilecompletionnotificationmodes_func","winbase/SetFileCompletionNotificationModes"]
old-location: fs\setfilecompletionnotificationmodes_func.htm
tech.root: fs
ms.assetid: 23796484-ee47-4f80-856d-5a5d5635547c
ms.date: 12/05/2018
ms.keywords: FILE_SKIP_COMPLETION_PORT_ON_SUCCESS, FILE_SKIP_SET_EVENT_ON_HANDLE, SetFileCompletionNotificationModes, SetFileCompletionNotificationModes function [Files], fs.setfilecompletionnotificationmodes_func, winbase/SetFileCompletionNotificationModes
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetFileCompletionNotificationModes
 - winbase/SetFileCompletionNotificationModes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
api_name:
 - SetFileCompletionNotificationModes
---

# SetFileCompletionNotificationModes function


## -description

 Sets the  notification modes for a file handle, allowing you to  specify how completion notifications 
    work for the specified file.

## -parameters

### -param FileHandle [in]

A handle to the file.

### -param Flags [in]

The modes to be set.  One or more modes can be set at the same time; however, after a mode has been set for 
      a file handle, it cannot be removed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_SKIP_COMPLETION_PORT_ON_SUCCESS"></a><a id="file_skip_completion_port_on_success"></a><dl>
<dt><b>FILE_SKIP_COMPLETION_PORT_ON_SUCCESS</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
If the following three conditions are true, the I/O Manager does not queue a completion entry to the port, 
         when it would ordinarily do so. The conditions are:
         <ul>
<li>A completion port is associated with the file handle.</li>
<li>The file is opened for asynchronous I/O.</li>
<li>A request returns success immediately without returning 
           <b>ERROR_PENDING</b>.</li>
</ul>


When the <i>FileHandle</i> parameter is a socket, this mode is only compatible with 
         Layered Service Providers (LSP) that return Installable File Systems (IFS) handles. To detect whether a 
         non-IFS LSP is installed, use the 
         <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaenumprotocolsa">WSAEnumProtocols</a> function and examine the 
         <b>dwServiceFlag1</b> member in each returned 
         <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaprotocol_infoa">WSAPROTOCOL_INFO</a> structure. If the 
         <b>XP1_IFS_HANDLES</b> (0x20000) bit is cleared then the specified LSP is not an IFS LSP. 
         Vendors that have non-IFS LSPs are encouraged to migrate to the 
         <a href="/windows/desktop/FWP/windows-filtering-platform-start-page">Windows Filtering Platform</a> 
         (WFP).

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SKIP_SET_EVENT_ON_HANDLE"></a><a id="file_skip_set_event_on_handle"></a><dl>
<dt><b>FILE_SKIP_SET_EVENT_ON_HANDLE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The I/O Manager does not set the event for the file object if a request returns with a success code, or the 
         error returned is <b>ERROR_PENDING</b> and the function that is called is not a 
         synchronous function.

If an explicit event is provided for the request, it is still signaled.

</td>
</tr>
</table>

## -returns

Returns nonzero if successful or zero otherwise.

To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To compile an application that uses this function, define the <b>_WIN32_WINNT</b> macro 
    as 0x0600 or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>