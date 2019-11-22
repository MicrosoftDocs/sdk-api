---
UID: NF:fileapi.FindCloseChangeNotification
title: FindCloseChangeNotification function (fileapi.h)

description: Stops change notification handle monitoring.
old-location: fs\findclosechangenotification.htm
tech.root: FileIO
ms.assetid: 17ca915c-3891-41f0-8816-6ac31c957afe

ms.date: 12/05/2018
ms.keywords: FindCloseChangeNotification, FindCloseChangeNotification function [Files], _win32_findclosechangenotification, base.findclosechangenotification, fileapi/FindCloseChangeNotification, fs.findclosechangenotification, winbase/FindCloseChangeNotification
ms.topic: function
f1_keywords: 
 - "fileapi/FindCloseChangeNotification"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FindCloseChangeNotification
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FindCloseChangeNotification function


## -description


Stops change notification handle monitoring.


## -parameters




### -param hChangeHandle [in]

A handle to a change notification handle created by the 
<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



After the <b>FindCloseChangeNotification</b> function is called, the handle 
    specified by the <i>hChangeHandle</i> parameter cannot be used in subsequent calls to either the 
<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findnextchangenotification">FindNextChangeNotification</a> or 
<b>FindCloseChangeNotification</b> function.

Change notifications can also be used in the 
<a href="https://docs.microsoft.com/windows/desktop/Sync/wait-functions">wait functions</a>.

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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findfirstchangenotificationa">FindFirstChangeNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findnextchangenotification">FindNextChangeNotification</a>
 

 

