---
UID: NS:setupapi._SP_ALTPLATFORM_INFO_V3
title: "_SP_ALTPLATFORM_INFO_V3"
author: windows-driver-content
description: An SP_ALTPLATFORM_INFO structure specifies, for a given computer, the version of the operating system and the computer's processor architecture.
old-location: devinst\sp_altplatform_info.htm
old-project: devinst
ms.assetid: d9aba6c9-1b23-4ce0-b796-904b39bec3ac
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSP_ALTPLATFORM_INFO_V3, PSP_ALTPLATFORM_INFO, PSP_ALTPLATFORM_INFO structure pointer [Device and Driver Installation], SP_ALTPLATFORM_INFO, SP_ALTPLATFORM_INFO structure [Device and Driver Installation], SP_ALTPLATFORM_INFO_V3, _SP_ALTPLATFORM_INFO_V3, devinst.sp_altplatform_info, di-struct_54b56314-f153-4d55-903f-561c7649208e.xml, setupapi/PSP_ALTPLATFORM_INFO, setupapi/SP_ALTPLATFORM_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
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
req.typenames: SP_ALTPLATFORM_INFO_V3, *PSP_ALTPLATFORM_INFO_V3
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Setupapi.h
api_name:
-	SP_ALTPLATFORM_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _SP_ALTPLATFORM_INFO_V3 structure


## -description


An SP_ALTPLATFORM_INFO structure specifies, for a given computer, the version of the operating system and the computer's processor architecture.


## -struct-fields




### -field cbSize

Specifies the size, in bytes, of an SP_ALTPLATFORM_INFO structure. Starting with Windows XP, the cbSize member of this structure must be set to <b>sizeof(</b>SP_ALTPLATFORM_INFO_V2<b>)</b>. For all earlier versions of Windows, the cbSize member of this structure must be set to <b>sizeof(</b>SP_ALTPLATFORM_INFO_V1<b>)</b>.


### -field Platform

Specifies one of the following operating system constants.

<table>
<tr>
<th>Platform constant</th>
<th>Meaning</th>
</tr>
<tr>
<td>
VER_PLATFORM_WIN32_WINDOWS

</td>
<td>
Windows 95/98/Millennium (Me) versions

</td>
</tr>
<tr>
<td>
VER_PLATFORM_WIN32_NT

</td>
<td>
Windows NT 4.0 and later versions of the NT-based operating system

</td>
</tr>
</table>
 


### -field MajorVersion

Specifies the major version number of the operating system.


### -field MinorVersion

Specifies the minor version number of the operating system.


### -field ProcessorArchitecture

Specifies one of the following processor architecture constants.

<table>
<tr>
<th>Processor architecture constant</th>
<th>Meaning</th>
</tr>
<tr>
<td>
PROCESSOR_ARCHITECTURE_INTEL

</td>
<td>
The alternative platform is an x86-based processor architecture.

</td>
</tr>
<tr>
<td>
PROCESSOR_ARCHITECTURE_AMD64

</td>
<td>
The alternative platform is an x64-based processor architecture.

</td>
</tr>
<tr>
<td>
PROCESSOR_ARCHITECTURE_IA64

</td>
<td>
The alternative platform is an Itanium-based processor architecture.

</td>
</tr>
<tr>
<td>
PROCESSOR_ARCHITECTURE_ALPHA

</td>
<td>
The alternative platform is an Alpha processor architecture that is running Windows NT 4.0. Only a system that is running Windows 2000 Print Server or Windows XP Professional Print Server can specify this value. 

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Reserved

Must be set to zero.


### -field DUMMYUNIONNAME.Flags

 


### -field FirstValidatedMajorVersion

 


### -field FirstValidatedMinorVersion

 


### -field ProductType

 


### -field SuiteMask

 


### -field BuildNumber

 




## -remarks



For information about the major and minor version numbers of the operating system, see the Microsoft Windows SDK documentation for <b>GetVersionEx</b> and OSVERSIONINFO.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551045">SetupDiGetActualSectionToInstallEx</a>
 

 

