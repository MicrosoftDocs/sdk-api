---
UID: NF:newdev.DiInstallDevice
title: DiInstallDevice function (newdev.h)
description: The DiInstallDevice function installs a specified driver that is preinstalled in the driver store on a specified device that is present in the system.
helpviewer_keywords: ["DiInstallDevice","DiInstallDevice function [Device and Driver Installation]","devinst.diinstalldevice","di-rtns_a2abff84-96e6-43c3-85ab-fe095d11b689.xml","newdev/DiInstallDevice"]
old-location: devinst\diinstalldevice.htm
tech.root: devinst
ms.assetid: e107fc37-02cb-4d50-822c-1c6fd80d7532
ms.date: 12/05/2018
ms.keywords: DiInstallDevice, DiInstallDevice function [Device and Driver Installation], devinst.diinstalldevice, di-rtns_a2abff84-96e6-43c3-85ab-fe095d11b689.xml, newdev/DiInstallDevice
req.header: newdev.h
req.include-header: Newdev.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
req.lib: Newdev.lib
req.dll: Newdev.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DiInstallDevice
 - newdev/DiInstallDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-newdev-config-l1-1-2.dll
 - Newdev.dll
 - Ext-MS-Win-Newdev-Config-L1-1-1.dll
api_name:
 - DiInstallDevice
---

# DiInstallDevice function


## -description

The <b>DiInstallDevice</b> function installs a specified driver that is preinstalled in the <a href="/windows-hardware/drivers/install/driver-store">driver store</a> on a specified device that is present in the system.

## -parameters

### -param hwndParent [in, optional]

A handle to the top-level window that <b>DiInstallDevice</b> uses to display any user interface component that is associated with installing the device. This parameter is optional and can be set to <b>NULL</b>.

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the specified device.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the specified device in the specified device information set.

### -param DriverInfoData [in, optional]

An pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure that specifies the driver to install on the specified device. This parameter is optional and can be set to <b>NULL</b>. If this parameter is <b>NULL</b>, <b>DiInstallDevice</b> searches the drivers preinstalled in the <a href="/windows-hardware/drivers/install/driver-store">driver store</a> for the driver that is the best match to the specified device, and, if one is found, installs the driver on the specified device.

### -param Flags [in]

A value of type <b>DWORD</b> that specifies zero or the following flag:





#### DIIDFLAG_SHOWSEARCHUI

If the caller does not specify a driver (<i>DriverInfoData</i> is set to <b>NULL</b>) and <b>DiInstallDevice</b> does not locate a preinstalled driver that matches the specified device. Instead, <b>DiInstallDevice</b> displays the Found New Hardware wizard for the device.



#### DIIDFLAG_NOFINISHINSTALLUI

<b>DiInstallDevice</b> does not start finish-install wizard pages or finish-install actions. The caller of <b>DiInstallDevice</b> must start these operations. The caller should only specify this flag if the caller requires that finish-install wizard pages be invoked in the context of a caller-supplied user interface component.



#### DIIDFLAG_INSTALLNULLDRIVER

<b>DiInstallDevice</b> attempts to install a <a href="/windows-hardware/drivers/">null driver</a> on the specified device. If this flag is set, <b>DiInstallDevice</b> does not use the <i>DriverInfoData</i> parameter. <b>DiInstallDevice</b> removes all device settings and, if the device cannot run in <a href="/windows-hardware/drivers/">raw mode</a>, the function sets the status of the device to <b>CM_PROB_FAILED_INSTALL</b>. If <b>DiInstallDevice</b> cannot install a null driver, the resulting state of the device is the same as if the device was connected for the first time to the computer and Windows did not locate a driver for the device.



#### DIIDFLAG_INSTALLCOPYINFDRIVERS

Any additional INF file specified via a <a href="/windows-hardware/drivers/install/inf-copyinf-directive">CopyINF</a> directive will be installed on any device it is applicable to.  Any failure in installing an additional INF will not cause the primary INF's installation to fail.

### -param NeedReboot [out, optional]

A pointer to a value of type <b>BOOL</b> that <b>DiInstallDevice</b> sets to indicate whether a system restart is required to complete the installation. This parameter is optional and can be set to <b>NULL</b>. If this parameter is supplied and a system restart is required to complete the installation, <b>DiInstallDevice</b> sets the value to <b>TRUE</b>. In this case, the caller is responsible for restarting the system. If this parameter is supplied and a system restart is not required, <b>DiInstallDevice</b> sets this parameter to <b>FALSE</b>. If this parameter is <b>NULL</b> and a system restart is required to complete the installation, <b>DiInstallDevice</b> displays a system restart dialog box.

## -returns

<b>DiInstallDevice</b> returns <b>TRUE</b> if the function successfully installed the specified driver on the specified device. Otherwise, <b>DiInstallDevice</b> returns <b>FALSE</b> and the logged error can be retrieved by making a call to <b>GetLastError</b>. Some of the more common error values that <b>GetLastError</b> might return are as follows:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have Administrator privileges. By default, Windows Vista and Windows Server 2008 require that a calling process have Administrator privileges to install a driver on a device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value that is specified for <i>Flags</i> is not zero or a bitwise OR of the valid flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IN_WOW64</b></dt>
</dl>
</td>
<td width="60%">
The calling application is a 32-bit application that is attempting to execute in a 64-bit environment, which is not allowed. For more information, see <a href="/windows-hardware/drivers/install/device-installations-on-64-bit-systems">Installing Devices on 64-Bit Systems</a>.

</td>
</tr>
</table>

## -remarks

Only call <b>DiInstallDevice</b> if it is necessary to install a specific driver on a specific device. Otherwise, use <a href="/windows/desktop/api/newdev/nf-newdev-updatedriverforplugandplaydevicesa">UpdateDriverForPlugAndPlayDevices</a> or <a href="/windows/desktop/api/newdev/nf-newdev-diinstalldrivera">DiInstallDriver</a> to install a driver for a device. For more information about which of these functions to call to install a driver on a device, see <a href="/windows-hardware/drivers/install/setupapi-functions-that-simplify-driver-installation">SetupAPI Functions that Simplify Driver Installation</a>. 

Before calling <b>DiInstallDevice</b>, the caller must obtain an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure to specify the device and, optionally, an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure to specify a driver for the device.

To create a device information set that contains the specified device and to obtain an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure for the device, do one of the following:

<ul>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a> to retrieve a device information set that contains the device and then call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a> to enumerate the devices in the device information set. On each call, <b>SetupDiEnumDeviceInfo</b> returns an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the enumerated device in the device information set. To obtain specific information about the enumerated device, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a> and supply the <b>SP_DEVINFO_DATA</b> structure that is returned by <b>SetupDiEnumDeviceInfo</b>. 

- OR -

</li>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinfoa">SetupDiOpenDeviceInfo</a> to add a device with a known device instance ID to the device information set. <b>SetupDiOpenDeviceInfo</b> returns an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the device in the device information set.

</li>
</ul>
To retrieve an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_drvinfo_data_v1_a">SP_DRVINFO_DATA</a> structure for a selected driver, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a> to build a list of drivers for the device and then call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdriverinfoa">SetupDiEnumDriverInfo</a> to enumerate the elements of the driver list for the device. For each enumerated driver, <b>SetupDiEnumDriverInfo</b> retrieves an <b>SP_DRVINFO_DATA</b> structure that identifies the driver. <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinfodetaila">SetupDiGetDriverInfoDetail</a> can also be called to retrieve additional detail about an enumerated driver. 

In general, an installation application should set <i>NeedReboot</i> to <b>NULL</b>. This ensures that <b>DiInstallDevice</b> prompts the user to restart the system if a restart is required to complete the installation. An application should supply a <i>NeedReboot</i> pointer only in the following cases:

<ul>
<li>
The application must call <b>DiInstallDevice</b> several times to complete an installation. In this case, the application should record whether a <b>TRUE</b><i>NeedReboot</i> value is returned by any of the calls to <b>DiInstallDevice </b> and, if so, prompt the user to restart the system after the final call to <b>DiInstallDevice</b> returns.

</li>
<li>
The application must perform required operations, other than calling <b>DiInstallDevice</b>, before a system restart should occur. If a system restart is required, the application should finish the required operations and then prompt the user to restart the system.

</li>
<li>
The application is a class installer, in which case, the class installer should set the <b>DI_NEEDREBOOT</b> flag in the <b>Flags</b> member of the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure for a device.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/newdev/nf-newdev-diinstalldrivera">DiInstallDriver</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdibuilddriverinfolist">SetupDiBuildDriverInfoList</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdriverinfoa">SetupDiEnumDriverInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinfodetaila">SetupDiGetDriverInfoDetail</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinfoa">SetupDiOpenDeviceInfo</a>



<a href="/windows/desktop/api/newdev/nf-newdev-updatedriverforplugandplaydevicesa">UpdateDriverForPlugAndPlayDevices</a>