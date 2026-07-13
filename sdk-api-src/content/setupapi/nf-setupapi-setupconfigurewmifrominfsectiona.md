---
UID: NF:setupapi.SetupConfigureWmiFromInfSectionA
title: SetupConfigureWmiFromInfSectionA function (setupapi.h)
description: The SetupConfigureWmiFromInfSection function configures the security of the WMI data that is exposed by an INF file when passed to the [DDInstall.WMI] section. (ANSI)
helpviewer_keywords: ["SCWMI_CLOBBER_SECURITY", "SetupConfigureWmiFromInfSectionA", "_setupapi_setupuninstalloeminf", "setupapi/SetupConfigureWmiFromInfSectionA"]
old-location: setup\setupconfigurewmifrominfsection.htm
tech.root: setup
ms.assetid: 1fcf9086-fde1-414c-9073-22452c3ffc6d
ms.date: 12/05/2018
ms.keywords: SCWMI_CLOBBER_SECURITY, SetupConfigureWmiFromInfSection, SetupConfigureWmiFromInfSection function [Setup API], SetupConfigureWmiFromInfSectionA, SetupConfigureWmiFromInfSectionW, _setupapi_setupuninstalloeminf, setup.setupconfigurewmifrominfsection, setupapi/SetupConfigureWmiFromInfSection, setupapi/SetupConfigureWmiFromInfSectionA, setupapi/SetupConfigureWmiFromInfSectionW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupConfigureWmiFromInfSectionW (Unicode) and SetupConfigureWmiFromInfSectionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupConfigureWmiFromInfSectionA
 - setupapi/SetupConfigureWmiFromInfSectionA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupConfigureWmiFromInfSection
 - SetupConfigureWmiFromInfSectionA
 - SetupConfigureWmiFromInfSectionW
---

# SetupConfigureWmiFromInfSectionA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupConfigureWmiFromInfSection</b> function configures the security of the WMI data that is exposed by an INF file when passed to the [DDInstall.WMI] section. 

It is used to establish security when the version of SetupAPI on the system does not natively support the WMI security information provided in the DDInstall section of the INF file.

## -parameters

### -param InfHandle [in]

A handle to an open INF file.

### -param SectionName [in]

Name of the section in the INF file that contains WMI security information. This should be in the form of[DDinstall.WMI].

### -param Flags [in]

This parameter can be set as follows.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCWMI_CLOBBER_SECURITY"></a><a id="scwmi_clobber_security"></a><dl>
<dt><b>SCWMI_CLOBBER_SECURITY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
If and only if this flag is set does the security information passed to this function override any security information set elsewhere in the INF file. If this flag does not exist and no security information exists in the INF file, the security is set. 

</td>
</tr>
</table>

## -returns

This function returns WINSETUPAPI BOOL.

## -remarks

In previous SetupAPI versions, WMI information in INF files is exposed to all users, and access could only be limited by correctly writing binary data to a registry key. Current versions read and process WMI security information provided by the DDInstall section of an INF file. 





> [!NOTE]
> The setupapi.h header defines SetupConfigureWmiFromInfSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/SetupApi/specifying-a-security-descriptor-from-an-inf-file">Specifying a Security Descriptor From an INF File</a>
