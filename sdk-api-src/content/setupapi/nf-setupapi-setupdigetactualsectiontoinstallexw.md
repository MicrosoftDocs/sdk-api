---
UID: NF:setupapi.SetupDiGetActualSectionToInstallExW
title: SetupDiGetActualSectionToInstallExW function (setupapi.h)
description: The SetupDiGetActualSectionToInstallEx function retrieves the name of the INF DDInstall section that installs a device for a specified operating system and processor architecture. (Unicode)
helpviewer_keywords: ["SetupDiGetActualSectionToInstallEx", "SetupDiGetActualSectionToInstallEx function [Device and Driver Installation]", "SetupDiGetActualSectionToInstallExW", "devinst.setupdigetactualsectiontoinstallex", "di-rtns_d8baadc3-b6eb-49cb-a8ca-e3f877c2e8e7.xml", "setupapi/SetupDiGetActualSectionToInstallEx"]
old-location: devinst\setupdigetactualsectiontoinstallex.htm
tech.root: devinst
ms.assetid: 0f05e3ec-09ea-4d9a-99c9-ddbc16753481
ms.date: 12/05/2018
ms.keywords: SetupDiGetActualSectionToInstallEx, SetupDiGetActualSectionToInstallEx function [Device and Driver Installation], SetupDiGetActualSectionToInstallExA, SetupDiGetActualSectionToInstallExW, devinst.setupdigetactualsectiontoinstallex, di-rtns_d8baadc3-b6eb-49cb-a8ca-e3f877c2e8e7.xml, setupapi/SetupDiGetActualSectionToInstallEx
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiGetActualSectionToInstallExW
 - setupapi/SetupDiGetActualSectionToInstallExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiGetActualSectionToInstallEx
 - SetupDiGetActualSectionToInstallExW
---

# SetupDiGetActualSectionToInstallExW function


## -description

The <b>SetupDiGetActualSectionToInstallEx</b> function retrieves the name of the <a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall section</a> that installs a device for a specified operating system and processor architecture.

## -parameters

### -param InfHandle [in]

A handle to the INF file that contains the <i>DDInstall</i> section.

### -param InfSectionName [in]

A pointer to the <i>DDInstall</i> section name (as specified in an <a href="/windows-hardware/drivers/install/inf-models-section">INF Models section</a>). The maximum length of the section name, in characters, is 254.

### -param AlternatePlatformInfo [in, optional]

A pointer, if non-<b>NULL</b>, to an <a href="/windows/win32/api/setupapi/ns-setupapi-sp_altplatform_info_v2">SP_ALTPLATFORM_INFO</a> structure. This structure is used to specify an operating system and processor architecture that is different from that on the local computer. To return the <i>DDInstall</i> section name for the local computer, set this parameter to <b>NULL</b>. Otherwise, provide an SP_ALTPLATFORM structure and set its members as follows:





#### cbSize

Set to the size, in bytes, of an SP_ALTPLATFORM_INFO structure.



#### Platform

Set to VER_PLATFORM_WIN32_NT for Windows XP and later versions of Windows.



#### MajorVersion

Not used.



#### MinorVersion

Not Used.



#### ProcessorArchitecture

Set one of the following processor architecture constants.

<table>
<tr>
<th>Processor Architecture Constant</th>
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
PROCESSOR_ARCHITECTURE_IA64

</td>
<td>
The alternative platform is an Itanium-based processor architecture.

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
</table>
 



#### Reserved

Set to zero.

### -param InfSectionWithExt [out, optional]

A pointer to a character buffer to receive the <i>DDInstall</i> section name, its platform extension, and a NULL terminator. This is the decorated section name that should be used for installation.  If this parameter is <b>NULL</b>, the function returns <b>TRUE</b> and sets <i>RequiredSize</i> to the size, in characters, that is required to return the <i>DDInstall</i> section name, its platform extension, and a terminating NULL character.

### -param InfSectionWithExtSize [in]

The size, in characters, of the buffer that is pointed to by the <i>InfSectionWithExt</i> parameter. The maximum length of a NULL-terminated INF section name, in characters, is MAX_INF_SECTION_NAME_LENGTH.

### -param RequiredSize [out, optional]

A pointer to the variable that receives the size, in characters, that is required to return the <i>DDInstall</i> section name, the platform extension, and a terminating NULL character.

### -param Extension [out, optional]

A pointer to a variable that receives a pointer to the '.' character that marks the start of the extension in the <i>InfSectionWithExt</i> buffer. If the <i>InfSectionWithExt</i> buffer is not supplied or is too small, this parameter is not set. Set this parameter to <b>NULL</b> if a pointer to the extension is not required.

### -param Reserved

Reserved for internal use only. Must be set to <b>NULL</b>.


##### - AlternatePlatformInfo.MajorVersion

Not used.


##### - AlternatePlatformInfo.MinorVersion

Not Used.


##### - AlternatePlatformInfo.Platform

Set to VER_PLATFORM_WIN32_NT for Windows XP and later versions of Windows.


##### - AlternatePlatformInfo.ProcessorArchitecture

Set one of the following processor architecture constants.

<table>
<tr>
<th>Processor Architecture Constant</th>
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
PROCESSOR_ARCHITECTURE_IA64

</td>
<td>
The alternative platform is an Itanium-based processor architecture.

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
</table>
 


##### - AlternatePlatformInfo.Reserved

Set to zero.


##### - AlternatePlatformInfo.cbSize

Set to the size, in bytes, of an SP_ALTPLATFORM_INFO structure.

## -returns

If the function is successful, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupDiGetActualSectionToInstallEx</b> is an extended form of <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetactualsectiontoinstalla">SetupDiGetActualSectionToInstall</a>. These functions support the extensions to <i>DDInstall</i> section names that are used to specify OS-specific and architecture-specific installation actions for a device. For information about these extensions, see <a href="/windows-hardware/drivers/install/creating-inf-files-for-multiple-platforms-and-operating-systems">Creating INF Files for Multiple Platforms and Operating Systems</a>.

If you do not supply alternative platform information with a call to <b>SetupDiGetActualSectionToInstallEx</b>, the function performs the same operation as <b>SetupDiGetActualSectionToInstall</b>. The latter function searches for the specified install section name using the platform information for the local computer.

If you supply alternative platform information with a call to <b>SetupDiGetActualSectionToInstallEx</b>, the function does the following:

<ul>
<li>
If you specify a platform of VER_PLATFORM_WIN32_NT, the function first searches in the specified INF file for a decorated install section name that matches the name, operating system, and processor architecture that you specify. If, for example, you specify an install section name of <b>InstallSec</b>, the function searches for one of the following decorated names, depending on the specified processor architecture:<ul>
<li>If you specify the x86-based processor architecture, the function searches for the decorated name <b>InstallSec.ntx86</b>.</li>
<li>If you specify the x64-based processor architecture, the function searches for the decorated name <b>InstallSec.ntamd64</b>.</li>
<li>If you specify the Itanium-based processor architecture, the function searches for the decorated name <b>InstallSec.ntia64</b>.</li>
</ul>


If the function finds a match for the name, operating system, and processor architecture, it terminates the search and returns the corresponding decorated name. If the function does not find such a match, the function searches for a section whose name is <b>InstallSec.nt</b>. If the function finds a match for <b>InstallSec.nt</b>, it terminates the search and returns this name. If the function does not find a match for either of the above searches, it returns <b>InstallSec</b>, but does not verify that the INF file contains an install section whose name is <b>InstallSec</b>.

</li>
</ul>




> [!NOTE]
> The setupapi.h header defines SetupDiGetActualSectionToInstallEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall Section</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetactualsectiontoinstallexa">SetupDiGetActualSectionToInstallEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a>
