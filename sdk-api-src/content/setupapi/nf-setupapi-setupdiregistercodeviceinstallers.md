---
UID: NF:setupapi.SetupDiRegisterCoDeviceInstallers
title: SetupDiRegisterCoDeviceInstallers function (setupapi.h)
description: The SetupDiRegisterCoDeviceInstallers function is the default handler for DIF_REGISTER_COINSTALLERS.
helpviewer_keywords: ["SetupDiRegisterCoDeviceInstallers","SetupDiRegisterCoDeviceInstallers function [Device and Driver Installation]","devinst.setupdiregistercodeviceinstallers","di-rtns_03f0dc0a-f133-4280-b32d-9a811d04a844.xml","setupapi/SetupDiRegisterCoDeviceInstallers"]
old-location: devinst\setupdiregistercodeviceinstallers.htm
tech.root: devinst
ms.assetid: 75d0275b-9eb8-45ec-ac8e-b18d59e0c011
ms.date: 12/05/2018
ms.keywords: SetupDiRegisterCoDeviceInstallers, SetupDiRegisterCoDeviceInstallers function [Device and Driver Installation], devinst.setupdiregistercodeviceinstallers, di-rtns_03f0dc0a-f133-4280-b32d-9a811d04a844.xml, setupapi/SetupDiRegisterCoDeviceInstallers
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
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiRegisterCoDeviceInstallers
 - setupapi/SetupDiRegisterCoDeviceInstallers
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
 - SetupDiRegisterCoDeviceInstallers
---

# SetupDiRegisterCoDeviceInstallers function


## -description

The <b>SetupDiRegisterCoDeviceInstallers</b> function is the default handler for <a href="/windows-hardware/drivers/install/dif-register-coinstallers">DIF_REGISTER_COINSTALLERS</a>.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to register co-installers. The device information set must not contain any remote elements.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.

## -returns

<b>SetupDiRegisterCoDeviceInstallers</b> returns <b>TRUE</b> if the function succeeds. If the function returns <b>FALSE</b>, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> for extended error information.

## -remarks

The caller of <b>SetupDiRegisterCoDeviceInstallers</b> must be a member of the Administrators group.

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiRegisterCoDeviceInstallers</b> and only in those situations where the class installer must perform co-installer registration operations after <b>SetupDiRegisterCoDeviceInstallers</b> completes the default co-installer registration operation. In such situations, the class installer must directly call <b>SetupDiRegisterCoDeviceInstallers</b> when the installer processes a DIF_REGISTER_COINSTALLERS request. For more information about calling the default handler, see <a href="/windows-hardware/drivers/install/calling-the-default-dif-code-handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
<b>SetupDiRegisterCoDeviceInstallers</b> reads the INF file for the device specified by <i>DeviceInfoData</i> and creates registry entries to register any device-specific co-installers listed in the INF file. Co-installers are listed in an <a href="/windows-hardware/drivers/install/inf-ddinstall-coinstallers-section">INF DDInstall.CoInstallers section</a>. This function also copies the files for the co-installers, unless the DI_NOFILECOPY flag is set. 

If there is no driver selected, or the device has an INF file for Windows 9x or Millennium Edition, this function does not register any co-installers.

Registering a new device-specific co-installer invalidates the Device Installer's current list of co-installers. After a successful registration, the Device Installer updates its list of co-installers.

This function only registers device-specific co-installers, not class co-installers. 

For more information about how to write and register device-specific co-installers, see <a href="/windows-hardware/drivers/install/writing-a-co-installer">Writing a Co-installer</a>.

The device information set specified by <i>DeviceInfoSet</i> must only contain elements on the local computer.

## -see-also

<a href="/windows-hardware/drivers/install/dif-register-coinstallers">DIF_REGISTER_COINSTALLERS</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>