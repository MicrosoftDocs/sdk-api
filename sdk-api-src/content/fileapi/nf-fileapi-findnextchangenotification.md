---
UID: NF:fileapi.FindNextChangeNotification
title: FindNextChangeNotification function (fileapi.h)
description: Requests that the operating system signal a change notification handle the next time it detects an appropriate change.
helpviewer_keywords: ["FindNextChangeNotification","FindNextChangeNotification function [Files]","_win32_findnextchangenotification","base.findnextchangenotification","fileapi/FindNextChangeNotification","fs.findnextchangenotification","winbase/FindNextChangeNotification"]
old-location: fs\findnextchangenotification.htm
tech.root: fs
ms.assetid: 0f93cc96-6e3b-4c03-aa5a-7a74d054a7ff
ms.date: 12/05/2018
ms.keywords: FindNextChangeNotification, FindNextChangeNotification function [Files], _win32_findnextchangenotification, base.findnextchangenotification, fileapi/FindNextChangeNotification, fs.findnextchangenotification, winbase/FindNextChangeNotification
req.header: fileapi.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindNextChangeNotification
 - fileapi/FindNextChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FindNextChangeNotification
---

# FindNextChangeNotification function


## -description

Requests that the operating system signal a change notification handle the next time it detects an appropriate change.

## -parameters

### -param hChangeHandle [in]

A handle to a change notification handle created by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After the 
<b>FindNextChangeNotification</b> function returns successfully, the application can wait for notification that a change has occurred by using the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>.

If a change occurs after a call to 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a> but before a call to 
<b>FindNextChangeNotification</b>, the operating system records the change. When 
<b>FindNextChangeNotification</b> is executed, the recorded change immediately satisfies a wait for the change notification.

Each successful call to **FindNextChangeNotification** must be followed by a call to one of the wait functions. If the wait function returns for any reason other than the change notification handle being signaled (for example, if the wait times out), the application must retry the wait. Failing to follow this rule can cause the system to eventually run out of resources. It can also cause the application to miss some change notifications.

When <i>hChangeHandle</i> is no longer needed, close it by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findclosechangenotification">FindCloseChangeNotification</a> function.

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
See remark

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
 

Application might experience false positives on CsvFs pause/resume.


#### Examples

For an example, see 
<a href="/windows/desktop/FileIO/obtaining-directory-change-notifications">Obtaining Directory Change Notifications</a>. 
            

<div class="code"></div>

## -see-also

<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclosechangenotification">FindCloseChangeNotification</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a>