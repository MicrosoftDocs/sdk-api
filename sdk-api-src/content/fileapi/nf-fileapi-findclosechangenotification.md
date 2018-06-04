---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# FindCloseChangeNotification function


## -description


Stops change notification handle monitoring.


## -parameters




### -param hChangeHandle [in]

A handle to a change notification handle created by the 
<a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After the <b>FindCloseChangeNotification</b> function is called, the handle 
    specified by the <i>hChangeHandle</i> parameter cannot be used in subsequent calls to either the 
<a href="https://msdn.microsoft.com/0f93cc96-6e3b-4c03-aa5a-7a74d054a7ff">FindNextChangeNotification</a> or 
<b>FindCloseChangeNotification</b> function.

Change notifications can also be used in the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>.

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




<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/dde4dd17-0f8c-41b5-8685-4e4c6b3def3c">FindFirstChangeNotification</a>



<a href="https://msdn.microsoft.com/0f93cc96-6e3b-4c03-aa5a-7a74d054a7ff">FindNextChangeNotification</a>
 

 

