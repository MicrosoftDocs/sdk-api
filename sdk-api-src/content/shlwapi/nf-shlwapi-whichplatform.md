---
UID: NF:shlwapi.WhichPlatform
title: WhichPlatform function
author: windows-sdk-content
description: WhichPlatform may be altered or unavailable.
old-location: shell\WhichPlatform.htm
tech.root: shell
ms.assetid: 14af733b-81b4-40a2-b93b-6f387b181f12
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WhichPlatform, WhichPlatform function [Windows Shell], _win32_WhichPlatform, shell.WhichPlatform, shlwapi/WhichPlatform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
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
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - WhichPlatform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WhichPlatform function


## -description


<p class="CCE_Message">[<b>WhichPlatform</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves a value that indicates the type of Shell32.dll that the platform contains.


## -parameters






## -returns



Type: <b>UINT</b>

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLATFORM_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The function was unable to determine the Shell32.dll version.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLATFORM_IE3</b></dt>
</dl>
</td>
<td width="60%">
Obsolete: Use PLATFORM_BROWSERONLY.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLATFORM_BROWSERONLY</b></dt>
</dl>
</td>
<td width="60%">
The Shell32.dll version is browser-only, with no new shell.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLATFORM_INTEGRATED</b></dt>
</dl>
</td>
<td width="60%">
The platform contains an integrated shell.

</td>
</tr>
</table>
 




## -remarks



This function always returns PLATFORM_INTEGRATED because Windows XP comes with an integrated shell.




## -see-also




<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Shell and Common Controls Versions</a>
 

 

