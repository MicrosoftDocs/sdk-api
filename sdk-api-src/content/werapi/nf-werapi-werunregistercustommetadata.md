---
UID: NF:werapi.WerUnregisterCustomMetadata
title: WerUnregisterCustomMetadata function
author: windows-sdk-content
description: Removes an item of app-specific metadata being collected during error reporting for the application.
old-location: wer\werunregistercustommetadata.htm
old-project: wer
ms.assetid: 29DB2CE5-2A96-450B-96C8-082B786613F9
ms.author: windowssdkdev
ms.date: 03/22/2018
ms.keywords: WerUnRegisterCustomMetadata, WerUnRegisterCustomMetadata function [Windows Error Reporting], WerUnregisterCustomMetadata, wer.werunregistercustommetadata, werapi/WerUnRegisterCustomMetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
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
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerUnRegisterCustomMetadata
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerUnregisterCustomMetadata function


## -description


Removes an item of app-specific metadata being collected during error reporting for the application.


## -parameters




### -param key

The "key" string for the metadata element being removed. It must have been previously registered with the <a href="https://msdn.microsoft.com/55FB3110-314A-4327-AA8F-3AF77B7006DD">WerRegisterCustomMetadata</a> function.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The process state is not valid. For example, the process is in <a href="https://msdn.microsoft.com/9357786c-1992-4e28-ac75-c2dfda1df7f1">application recovery mode</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
WER could not find the metadata item to remove.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/55FB3110-314A-4327-AA8F-3AF77B7006DD">WerRegisterCustomMetadata</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

