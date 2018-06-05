---
UID: NF:fileapi.FindNextChangeNotification
title: FindNextChangeNotification function
author: windows-sdk-content
description: Requests that the operating system signal a change notification handle the next time it detects an appropriate change.
old-location: fs\findnextchangenotification.htm
old-project: FileIO
ms.assetid: 0f93cc96-6e3b-4c03-aa5a-7a74d054a7ff
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: FindNextChangeNotification, FindNextChangeNotification function [Files], _win32_findnextchangenotification, base.findnextchangenotification, fileapi/FindNextChangeNotification, fs.findnextchangenotification, winbase/FindNextChangeNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: STREAM_INFO_LEVELS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-File-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-File-l1-2-0.dll
-	API-MS-Win-Core-File-l1-2-1.dll
-	API-MS-Win-Core-File-l1-2-2.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	FindNextChangeNotification
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 5
---

# FindNextChangeNotification function


## -description


Requests that the operating system signal a change notification handle the next time it detects an appropriate change.


## -parameters




### -param hChangeHandle [in]

A handle to a change notification handle created by the 
<a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After the 
<b>FindNextChangeNotification</b> function returns successfully, the application can wait for notification that a change has occurred by using the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>.

If a change occurs after a call to 
<a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a>
       but before a call to 
<b>FindNextChangeNotification</b>, the operating system records the change. When 
<b>FindNextChangeNotification</b> is executed, the recorded change immediately satisfies a wait for the change notification.

<b>FindNextChangeNotification</b> should not be used more than once on the same handle without using one of the wait functions. An application may miss a change notification if it uses 
<b>FindNextChangeNotification</b> when there is a change request outstanding. 

When <i>hChangeHandle</i> is no longer needed, close it by using the 
<a href="https://msdn.microsoft.com/17ca915c-3891-41f0-8816-6ac31c957afe">FindCloseChangeNotification</a> function.

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
<a href="https://msdn.microsoft.com/ad884b15-e040-478b-aa99-d8622198f62a">Obtaining Directory Change Notifications</a>. 
            

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/17ca915c-3891-41f0-8816-6ac31c957afe">FindCloseChangeNotification</a>



<a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a>
 

 

