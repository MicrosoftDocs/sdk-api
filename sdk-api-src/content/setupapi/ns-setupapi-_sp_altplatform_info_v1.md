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

# _SP_ALTPLATFORM_INFO_V1 structure


## -description


This structure is used to pass information for an alternate platform to 
<a href="https://msdn.microsoft.com/bc7c08ff-3d6b-4d45-b634-1358302f6fc6">SetupQueryInfOriginalFileInformation</a>.

Setup implicitly uses the <b>SP_ALTPLATFORM_INFO_V1</b> structure if USE_SP_ALTPLATFORM_INFO_V1 is set to 1 or if _WIN32_WINNT is less than or equal to 0x500. This version is for use with Windows 2000.

Setup implicitly uses the <a href="https://msdn.microsoft.com/eb66ef5a-212d-4224-87b5-d64e8e188139">SP_ALTPLATFORM_INFO_V2</a> structure if USE_SP_ALTPLATFORM_INFO_V1 is 0 or undefined and _WIN32_WINNT is set to 0x501. 


## -struct-fields




### -field cbSize

Size of this structure, in bytes.


### -field Platform

Operating system. This must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORM_WIN32_WINDOWS"></a><a id="ver_platform_win32_windows"></a><dl>
<dt><b>VER_PLATFORM_WIN32_WINDOWS</b></dt>
</dl>
</td>
<td width="60%">
Legacy operating systems.

</td>
</tr>
<tr>
<td width="40%"><a id="VER_PLATFORM_WIN32_NT"></a><a id="ver_platform_win32_nt"></a><dl>
<dt><b>VER_PLATFORM_WIN32_NT</b></dt>
</dl>
</td>
<td width="60%">
Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, or Windows 2000.

</td>
</tr>
</table>
 


### -field MajorVersion

Major version of the operating system.


### -field MinorVersion

Minor version of the operating system.


### -field ProcessorArchitecture

Processor architecture. This must be PROCESSOR_ARCHITECTURE_INTEL, PROCESSOR_ARCHITECTURE_ALPHA, PROCESSOR_ARCHITECTURE_IA64, PROCESSOR_ARCHITECTURE_ALPHA64.


### -field Reserved

Must be set to zero.


## -see-also




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/eb66ef5a-212d-4224-87b5-d64e8e188139">SP_ALTPLATFORM_INFO_V2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

