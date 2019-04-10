---
UID: NF:werapi.WerRegisterAppLocalDump
title: WerRegisterAppLocalDump function (werapi.h)
author: windows-sdk-content
description: Registers a path relative to the local app store for the calling application where Windows Error Reporting (WER) should save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding.
old-location: wer\werregisterapplocaldump.htm
tech.root: wer
ms.assetid: C57F5758-2BF7-444E-A22C-62C925B899A1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WerRegisterAppLocalDump, WerRegisterAppLocalDump function [Windows Error Reporting], wer.werregisterapplocaldump, werapi/WerRegisterAppLocalDump
ms.topic: function
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
req.dll: KernelBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KernelBase.dll
 - Kernel32.dll
 - Api-ms-win-core-windowserrorreporting-l1.dll
api_name:
 - WerRegisterAppLocalDump
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerRegisterAppLocalDump function


## -description


Registers a path relative to the local app store for the calling application where Windows Error Reporting (WER) should save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding.


## -parameters




### -param localAppDataRelativePath [in]

The path relative to the local app store for the calling application where WER should save a copy of the diagnostic memory dump that WER collects when one of the processes for the application stops responding. The maximum length for this relative path in characters is <b>WER_MAX_LOCAL_DUMP_SUBPATH_LENGTH</b>, which has a value of 64. This maximum length includes the null-termination character.


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
The process cannot store the memory dump, or WER cannot create a location to store the memory dump.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>localAppDataRelativePath</i> parameter is NULL or is longer than 64 characters.

</td>
</tr>
</table>
 




## -remarks



A packaged application calls <b>WerRegisterAppLocalDump</b> when the application launches to request a copy of the diagnostic memory dump that WER collects  if or when one of the processes  for the application stops responding.

WER does not manage storage at the location that the relative path specifies or the number of memory dumps that are collected for the application.




## -see-also




<a href="https://msdn.microsoft.com/A3AD976A-9C44-494C-ABF0-90D151001E30">WerUnregisterAppLocalDump</a>
 

 

