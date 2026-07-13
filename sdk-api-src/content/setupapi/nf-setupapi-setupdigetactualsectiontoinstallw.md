---
UID: NF:setupapi.SetupDiGetActualSectionToInstallW
title: SetupDiGetActualSectionToInstallW function (setupapi.h)
description: The SetupDiGetActualSectionToInstall function retrieves the appropriate INF DDInstall section to use when installing a device from a device INF file on a local computer. (Unicode)
helpviewer_keywords: ["SetupDiGetActualSectionToInstall", "SetupDiGetActualSectionToInstall function [Device and Driver Installation]", "SetupDiGetActualSectionToInstallW", "devinst.setupdigetactualsectiontoinstall", "di-rtns_fce32f02-ef7f-4a51-a559-5f0da3738906.xml", "setupapi/SetupDiGetActualSectionToInstall"]
old-location: devinst\setupdigetactualsectiontoinstall.htm
tech.root: devinst
ms.assetid: ccb5e1a4-e6c3-48e5-ac25-b9b5504a03d7
ms.date: 12/05/2018
ms.keywords: SetupDiGetActualSectionToInstall, SetupDiGetActualSectionToInstall function [Device and Driver Installation], SetupDiGetActualSectionToInstallA, SetupDiGetActualSectionToInstallW, devinst.setupdigetactualsectiontoinstall, di-rtns_fce32f02-ef7f-4a51-a559-5f0da3738906.xml, setupapi/SetupDiGetActualSectionToInstall
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
 - SetupDiGetActualSectionToInstallW
 - setupapi/SetupDiGetActualSectionToInstallW
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
 - SetupDiGetActualSectionToInstall - SetupDiGetActualSectionToInstallW
---

# SetupDiGetActualSectionToInstallW function


## -description

The <b>SetupDiGetActualSectionToInstall</b> function retrieves the appropriate <a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall section</a> to use when installing a device from a device INF file on a local computer.

## -parameters

### -param InfHandle [in]

The handle to the INF file that contains the <i>DDInstall</i> section.

### -param InfSectionName [in]

A pointer to the <i>DDInstall</i> section name (as specified in an <a href="/windows-hardware/drivers/install/inf-models-section">INF Models section</a>). The maximum length of the section name, in characters, is 254.

### -param InfSectionWithExt [out, optional]

A pointer to a character buffer to receive the <i>DDInstall</i> section name, its platform extension, and a NULL terminator. This is the decorated section name that should be used for installation. If this parameter is <b>NULL</b>, <i>InfSectionWithExtSize</i> must be zero. If this parameter is <b>NULL</b>, the function returns <b>TRUE</b> and sets <i>RequiredSize</i> to the size, in characters, that is required to return the <i>DDInstall</i> section name, its platform extension, and a terminating NULL character.

### -param InfSectionWithExtSize [in]

The size, in characters, of the <i>InfSectionWithExt</i> buffer. If <i>InfSectionWithExt</i> is <b>NULL</b>, this parameter must be zero.

### -param RequiredSize [out, optional]

A pointer to the variable that receives the size, in characters, that is required to return the <i>DDInstall</i> section name, the platform extension, and a terminating NULL character.

### -param Extension [out, optional]

A pointer to a variable that receives a pointer to the '.' character that marks the start of the extension in the <i>InfSectionWithExt</i> buffer. If the <i>InfSectionWithExt</i> buffer is not supplied or is too small, this parameter is not set. Set this parameter to <b>NULL</b> if a pointer to the extension is not required.

## -returns

If the function is successful, it returns <b>TRUE</b>. If the function fails, it returns <b>FALSE</b>. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function supports the extensions to <i>DDInstall</i> section names that are used to specify OS-specific and architecture-specific installation behaviors for a device. For information about these extensions, see <a href="/windows-hardware/drivers/install/creating-inf-files-for-multiple-platforms-and-operating-systems">Creating INF Files for Multiple Platforms and Operating Systems</a>. <b>SetupDiGetActualSectionToInstall</b> searches for a <i>DDInstall</i> section name that matches the local computer in the manner described below.

The function first searches in the specified INF file for a decorated install section name that matches the specified name and has an extension that matches the operating system and processor architecture of the local computer. If, for example, you specify a section name of <b>InstallSec</b>, the function searches for one of the following decorated names, depending on the processor architecture of the local computer:

<ul>
<li>
For a computer that is based on the x86 processor architecture, the function searches for the decorated name <b>InstallSec.ntx86</b>.

</li>
<li>
For a computer that is based on the x64 processor architecture, the function searches for the decorated name <b>InstallSec.ntamd64</b>.

</li>
<li>
For a computer that is based on the Itanium processor architecture, the function searches for the decorated name <b>InstallSec.ntia64</b>.

</li>
</ul>
If the function finds a match for the name, operating system, and processor architecture, it terminates the search and returns the corresponding decorated name. If the function does not find such a match, the function searches for a section whose name is <b>InstallSec.NT</b>. If the function finds a match for <b>InstallSec.NT</b>, it terminates the search and returns this name. If the function does not find a match for either of the above searches, it returns <b>InstallSec</b>, but does not verify that the INF file contains an install section whose name is <b>InstallSec</b>.

The <i>DDInstall</i> section name is used as the base for <b>Hardware</b> and <b>Services</b> section names. For example, if the <i>DDInstall</i> section name that is found is <b>InstallSec.NTX86</b>, the <b>Services</b> section name must be named <b>InstallSec.NTX86.Services</b>.

The original <i>DDInstall</i> section name that is specified in the driver node is written to the driver's registry key's <b>InfSection</b> value entry. The extension that was found is stored in the key as the REG_SZ value <b>InfSectionExt</b>. For example:


```
InfSection       : REG_SZ :    "InstallSec"
InfSectionExt    : REG_SZ :    ".NTX86"
```


If a driver is not selected for the specified device information element, a null driver is installed. Upon return, the flags in the device's <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure indicate whether the system should be restarted or rebooted to cause the device to start.





> [!NOTE]
> The setupapi.h header defines SetupDiGetActualSectionToInstall as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall Section</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetactualsectiontoinstallexa">SetupDiGetActualSectionToInstallEx</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldevice">SetupDiInstallDevice</a>
