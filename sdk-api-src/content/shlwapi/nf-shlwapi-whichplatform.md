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
 

 

