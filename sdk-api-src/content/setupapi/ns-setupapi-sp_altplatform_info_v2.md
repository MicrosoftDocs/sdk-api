---
UID: NS:setupapi._SP_ALTPLATFORM_INFO_V2
title: SP_ALTPLATFORM_INFO_V2 (setupapi.h)
description: The SP_ALTPLATFORM_INFO_V2 structure is used to pass information for an alternate platform to SetupQueryInfOriginalFileInformation.
helpviewer_keywords: ["*PSP_ALTPLATFORM_INFO_V2","PSP_ALTPLATFORM_INFO_V2","PSP_ALTPLATFORM_INFO_V2 structure pointer [Setup API]","SP_ALTPLATFORM_INFO","SP_ALTPLATFORM_INFO_V2","SP_ALTPLATFORM_INFO_V2 structure [Setup API]","VER_PLATFORM_WIN32_NT","VER_PLATFORM_WIN32_WINDOWS","_setupapi_sp_altplatform_info","setup.sp_altplatform_info_v2","setupapi/PSP_ALTPLATFORM_INFO_V2","setupapi/SP_ALTPLATFORM_INFO_V2"]
old-location: setup\sp_altplatform_info_v2.htm
tech.root: setup
ms.assetid: eb66ef5a-212d-4224-87b5-d64e8e188139
ms.date: 12/05/2018
ms.keywords: '*PSP_ALTPLATFORM_INFO_V2, PSP_ALTPLATFORM_INFO_V2, PSP_ALTPLATFORM_INFO_V2 structure pointer [Setup API], SP_ALTPLATFORM_INFO, SP_ALTPLATFORM_INFO_V2, SP_ALTPLATFORM_INFO_V2 structure [Setup API], VER_PLATFORM_WIN32_NT, VER_PLATFORM_WIN32_WINDOWS, _setupapi_sp_altplatform_info, setup.sp_altplatform_info_v2, setupapi/PSP_ALTPLATFORM_INFO_V2, setupapi/SP_ALTPLATFORM_INFO_V2'
req.header: setupapi.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_ALTPLATFORM_INFO_V2, *PSP_ALTPLATFORM_INFO_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_ALTPLATFORM_INFO_V2
 - setupapi/_SP_ALTPLATFORM_INFO_V2
 - PSP_ALTPLATFORM_INFO_V2
 - setupapi/PSP_ALTPLATFORM_INFO_V2
 - SP_ALTPLATFORM_INFO_V2
 - setupapi/SP_ALTPLATFORM_INFO_V2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_ALTPLATFORM_INFO_V2
---

# SP_ALTPLATFORM_INFO_V2 structure


## -description

The <b>SP_ALTPLATFORM_INFO_V2</b> structure is used to pass information for an alternate platform to 
<a href="/windows/desktop/api/setupapi/nf-setupapi-setupqueryinforiginalfileinformationa">SetupQueryInfOriginalFileInformation</a>.

Setup  uses the <b>SP_ALTPLATFORM_INFO_V2</b> structure if USE_SP_ALTPLATFORM_INFO_V1 is 0 or undefined and _WIN32_WINNT is set to 0x501. <b>FirstValidatedMajorVersion</b> and <b>FirstValidatedMinorVersion</b> are only available with <b>SP_ALTPLATFORM_INFO_V2</b> and for use with Windows Server 2008, Windows Vista, Windows Server 2003,  or Windows XP.

Setup  uses the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v1">SP_ALTPLATFORM_INFO_V1</a> structure if USE_SP_ALTPLATFORM_INFO_V1 is set to 1 or if _WIN32_WINNT is less than or equal to 0x500. <b>FirstValidatedMajorVersion</b> and <b>FirstValidatedMinorVersion</b> are not available with <b>SP_ALTPLATFORM_INFO_V1</b>.

## -struct-fields

### -field cbSize

Size of this structure, in bytes.

### -field Platform

Operating system. This member must be one of the following values. 



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

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Reserved

### -field DUMMYUNIONNAME.Flags

 For Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP, this member must be set to SP_ALTPLATFORM_FLAGS_VERSION_RANGE to use <b>FirstValidatedMajorVersion</b> and <b>FirstValidatedMinorVersion</b>. This member must be set to zero for Windows 2000.

### -field FirstValidatedMajorVersion

Major version of the oldest previous operating system for which this package's digital signature is valid. For example, if the alternate platform is VER_PLATFORM_WIN32_NT, version 5.1, and you want a driver package signed with a 5.0 osattr to also be valid, set MajorVersion to 5, MinorVersion to 1, <b>FirstValidatedMajorVersion</b> to 5, and <b>FirstValidatedMinorVersion</b> 0. To validate packages signed for any previous operating system, specify 0 for these fields. To only validate against the target alternate platform, specify the same values as those in the MajorVersion and MinorVersion fields. Available with Windows XP or later only. The Flags member must be set to SP_ALTPLATFORM_FLAGS_VERSION_RANGE to use <b>FirstValidatedMajorVersion</b>.

### -field FirstValidatedMinorVersion

Minor version of the oldest previous operating system for which this package's digital signature is valid. For information see <b>FirstValidatedMajorVersion</b>. Available with Windows Server 2003 or Windows XP. The <b>Flags</b> member must be set to SP_ALTPLATFORM_FLAGS_VERSION_RANGE to use <b>FirstValidatedMinorVersion</b>.

## -see-also

<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_altplatform_info_v1">SP_ALTPLATFORM_INFO_V1</a>



<a href="/windows/desktop/SetupApi/structures--setup-api-">Structures</a>