---
UID: NF:setupapi.SetupDiInstallDevice
title: SetupDiInstallDevice function (setupapi.h)
description: The SetupDiInstallDevice function is the default handler for the DIF_INSTALLDEVICE installation request.
helpviewer_keywords: ["SetupDiInstallDevice","SetupDiInstallDevice function [Device and Driver Installation]","devinst.setupdiinstalldevice","di-rtns_5b8edbe1-3653-41c6-8a61-12f11544ff08.xml","setupapi/SetupDiInstallDevice"]
old-location: devinst\setupdiinstalldevice.htm
tech.root: devinst
ms.assetid: 130a58a8-7964-40cb-87e8-4765178bd1ff
ms.date: 12/05/2018
ms.keywords: SetupDiInstallDevice, SetupDiInstallDevice function [Device and Driver Installation], devinst.setupdiinstalldevice, di-rtns_5b8edbe1-3653-41c6-8a61-12f11544ff08.xml, setupapi/SetupDiInstallDevice
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
 - SetupDiInstallDevice
 - setupapi/SetupDiInstallDevice
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
 - SetupDiInstallDevice
---

# SetupDiInstallDevice function


## -description

The <b>SetupDiInstallDevice</b> function is the default handler for the <a href="/windows-hardware/drivers/install/dif-installdevice">DIF_INSTALLDEVICE</a> installation request.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> for the local system that contains a device information element that represents the device to install.

### -param DeviceInfoData [in, out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This is an IN-OUT parameter because <i>DeviceInfoData.</i><b>DevInst</b> might be updated with a new handle value upon return.

## -returns

The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupDiInstallDevice</b> installs a driver from the INF file. SetupAPI's definition of the "<i>driver</i>" is really a "<a href="/windows-hardware/drivers/">driver node</a>." Therefore, when this function installs a driver, it also installs the items in the following list:

<ul>
<li>
The service(s) for the device.

</li>
<li>
The driver files.

</li>
<li>
Device-specific co-installers (if any).

</li>
<li>
Property-page providers (if any).

</li>
<li>
Control-panel applets (if any).

</li>
</ul>
This function also registers any required device interfaces. 

A successful installation includes, but is not limited to, the following steps:

<ul>
<li>
Create a <a href="/windows-hardware/drivers/">driver key</a> in the registry and write appropriate entries (such as <b>InfPath</b> and <b>ProviderName</b>).

</li>
<li>
Locate and process the <a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall section</a> for the device. The section might be OS/architecture-specific. The <i>DDInstall</i> section's <b>AddReg</b> and <b>DelReg</b> entries are directed at the device's <a href="/windows-hardware/drivers/">software key</a>. Locate and process the <i>DDInstall</i><b>.HW</b> section whose <b>AddReg</b> and <b>DelReg</b> entries are directed at the device's <a href="/windows-hardware/drivers/">hardware key</a>. Locate and process the <a href="/windows-hardware/drivers/install/inf-ddinstall-logconfigoverride-section">INF DDInstall.LogConfigOverride section</a>, if present, to supply an <a href="/windows-hardware/drivers/kernel/hardware-resources">override configuration</a> for the device. Locate and process the <a href="/windows-hardware/drivers/install/inf-ddinstall-services-section">INF DDInstall.Services section</a> to add services for the device (and potentially remove any old services that are no longer necessary).

</li>
<li>
Copy the INF file to the system INF directory.

</li>
<li>
Possibly perform the other file operations, based on flag settings in the device installation parameters. 

If the DI_NOFILECOPY flag and the DI_NOVCP flag are <i>clear</i>, perform any file operations specified in the <i>DDInstall </i> section. If the DI_NOVCP flag is set, queue any file operations. 

If the DI_NOFILECOPY flag is set, do not copy the files. This flag might be set if, for example, a <a href="/windows-hardware/drivers/install/dif-installdevicefiles">DIF_INSTALLDEVICEFILES</a> operation was already performed for this device installation. 

</li>
<li>
Load the drivers for the device. This includes the function driver and any upper or lower-filter drivers.

</li>
<li>
Call the drivers' <a href="/windows-hardware/drivers/ddi/content/wdm/nc-wdm-driver_add_device">AddDevice</a> routines.

</li>
<li>
Start the device by sending an  <a href="/windows-hardware/drivers/kernel/irp-mn-start-device">IRP_MN_START_DEVICE</a> I/O request packet (IRP).

</li>
</ul>
Windows does not start the device if the DI_NEEDRESTART, DI_NEEDREBOOT, or DI_DONOTCALLCONFIGMG flag is set in the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure.

A class installer should return ERROR_DI_DO_DEFAULT or call this function when handling a <a href="/windows-hardware/drivers/install/dif-installdevice">DIF_INSTALLDEVICE</a> request. This function performs many tasks for device installation and that list of tasks might be expanded in future releases. If a class installer performs device installation without calling this function, the class installer might not work correctly on future versions of the operating system. 

If Windows cannot locate an INF file for the device, it will send DIF_INSTALLDEVICE in an attempt to install a <a href="/windows-hardware/drivers/">null driver</a>. <b>SetupDiInstallDevice</b> installs a null driver only if the device supports <a href="/windows-hardware/drivers/">raw mode</a> or is a non-PnP device (reported by <a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-ioreportdetecteddevice">IoReportDetectedDevice</a>). For more information, see <a href="/windows-hardware/drivers/install/dif-installdevice">DIF_INSTALLDEVICE</a>.

If the DI_FLAGSEX_SETFAILEDINSTALL flag is set in the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure, <b>SetupDiInstallDevice</b> just sets the FAILEDINSTALL flag in the device's <b>ConfigFlags</b> registry value.

<div class="alert"><b>Note</b>  Only a <a href="/windows-hardware/drivers/">class installer</a> should call <b>SetupDiInstallDevice</b> and only in those situations where the class installer must perform device installation operations after <b>SetupDiInstallDevice</b> completes the default device installation operation. In such situations, the class installer must directly call <b>SetupDiInstallDevice</b> when the installer processes a DIF_INSTALLDEVICE request. For more information about calling the default handler, see <a href="/windows-hardware/drivers/install/calling-the-default-dif-code-handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
The caller of <b>SetupDiInstallDevice</b> must be a member of the Administrators group.

## -see-also

<a href="/windows-hardware/drivers/install/dif-installdevice">DIF_INSTALLDEVICE</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldriverfiles">SetupDiInstallDriverFiles</a>