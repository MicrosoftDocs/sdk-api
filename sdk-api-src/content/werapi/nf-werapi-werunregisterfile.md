---
UID: NF:werapi.WerUnregisterFile
title: WerUnregisterFile function (werapi.h)
author: windows-sdk-content
description: Removes a file from the list of files to be added to reports generated for the current process.
old-location: wer\werunregisterfile.htm
tech.root: wer
ms.assetid: 2b2684a4-3030-4fae-ad1c-a60d13d2c643
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WerUnregisterFile, WerUnregisterFile function [Windows Error Reporting], base.werunregisterfile, wer.werunregisterfile, werapi/WerUnregisterFile
ms.topic: function
req.header: werapi.h
req.include-header: 
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
 - WerUnregisterFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerUnregisterFile function


## -description


Removes a file from the list of files to be added to reports generated for the current process.


## -parameters




### -param pwzFilePath [in]

The full path to the file. This file must have been registered using the <a href="https://msdn.microsoft.com/4b4bb1bb-6782-447a-901f-75702256d907">WerRegisterFile</a> function.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

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
The list of registered files does not contain the specified file.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/4b4bb1bb-6782-447a-901f-75702256d907">WerRegisterFile</a>



<a href="https://msdn.microsoft.com/5c076588-779c-4cd2-9fd9-1db3039e37a2">Windows Error Reporting</a>
 

 

