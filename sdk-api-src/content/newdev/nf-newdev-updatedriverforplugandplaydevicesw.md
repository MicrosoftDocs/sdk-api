---
UID: NF:newdev.UpdateDriverForPlugAndPlayDevicesW
title: UpdateDriverForPlugAndPlayDevicesW function (newdev.h)
description: Given an INF file and a hardware ID, the UpdateDriverForPlugAndPlayDevices function installs updated drivers for devices that match the hardware ID. (Unicode)
old-location: devinst\updatedriverforplugandplaydevices.htm
tech.root: devinst
ms.assetid: dd5022df-5b65-4ed4-ac54-68149df2c851
ms.date: 12/05/2018
ms.keywords: UpdateDriverForPlugAndPlayDevices, UpdateDriverForPlugAndPlayDevices function [Device and Driver Installation], UpdateDriverForPlugAndPlayDevicesA, UpdateDriverForPlugAndPlayDevicesW, devinst.updatedriverforplugandplaydevices, di-rtns_a9a559d4-7b81-4bd7-b6a7-f493787a3657.xml, newdev/UpdateDriverForPlugAndPlayDevices
req.header: newdev.h
req.include-header: Newdev.h
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
req.lib: Newdev.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UpdateDriverForPlugAndPlayDevicesW
 - newdev/UpdateDriverForPlugAndPlayDevicesW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-newdev-config-l1-1-2.dll
 - ext-ms-win-newdev-config-l1-1-1.dll
 - Newdev.lib
 - Newdev.dll
api_name:
 - UpdateDriverForPlugAndPlayDevices
---

# UpdateDriverForPlugAndPlayDevicesW function


## -description

Given an INF file and a <a href="/windows-hardware/drivers/install/hardware-ids">hardware ID</a>, the <b>UpdateDriverForPlugAndPlayDevices</b> function installs updated drivers for devices that match the hardware ID.

## -parameters

### -param hwndParent [in, optional]

A handle to the top-level window to use for any UI related to installing devices.

### -param HardwareId [in]

A pointer to a NULL-terminated string that supplies the hardware identifier to match existing devices on the computer. The maximum length of a NULL-terminated hardware identifier is MAX_DEVICE_ID_LEN. For more information about hardware identifiers, see <a href="/windows-hardware/drivers/install/device-identification-strings">Device Identification Strings</a>.

### -param FullInfPath [in]

A pointer to a NULL-terminated string that supplies the full path file name of an INF file. The files should be on the distribution media or in a vendor-created directory, not in a system location such as <i>%SystemRoot%\inf</i>. <b>UpdateDriverForPlugAndPlayDevices</b> copies driver files to the appropriate system locations if the installation is successful.

### -param InstallFlags [in]

A caller-supplied value created by using OR to combine zero or more of the following bit flags:





#### INSTALLFLAG_FORCE

If this flag is set and the function finds a device that matches the <i>HardwareId </i> value, the function installs new drivers for the device whether better drivers already exist on the computer. 

<div class="alert"><b>Important</b>  Use this flag only with extreme caution. Setting this flag can cause an older driver to be installed over a newer driver, if a user runs the vendor's application after newer drivers are available.</div>
<div> </div>


#### INSTALLFLAG_READONLY

If this flag is set, the function will not copy, rename, or delete any installation files. Use of this flag should be limited to environments in which file access is restricted or impossible, such as an "embedded" operating system.



#### INSTALLFLAG_NONINTERACTIVE

If this flag is set, the function will return <b>FALSE</b> when any attempt to display UI is detected. Set this flag only if the function will be called from a component (such as a service) that cannot display UI. 

<div class="alert"><b>Note</b>    If this flag is set and a UI display is attempted, the device can be left in an indeterminate state.</div>
<div> </div>
The <i>InstallFlags</i> parameter is typically zero.

### -param bRebootRequired [out, optional]

A pointer to a BOOL-typed variable that indicates whether a restart is required and who should prompt for it. This pointer is optional and can be <b>NULL</b>. 

If the pointer is <b>NULL</b>, <b>UpdateDriverForPlugAndPlayDevices</b> prompts for a restart after installing drivers, if necessary. If the pointer is supplied, the function returns a BOOLEAN value that is <b>TRUE</b> if the system should be restarted. It is then the caller's responsibility to prompt for a restart. 

For more information, see the following <b>Remarks</b> section.


##### - InstallFlags.INSTALLFLAG_FORCE

If this flag is set and the function finds a device that matches the <i>HardwareId </i> value, the function installs new drivers for the device whether better drivers already exist on the computer. 

<div class="alert"><b>Important</b>  Use this flag only with extreme caution. Setting this flag can cause an older driver to be installed over a newer driver, if a user runs the vendor's application after newer drivers are available.</div>
<div> </div>

##### - InstallFlags.INSTALLFLAG_NONINTERACTIVE

If this flag is set, the function will return <b>FALSE</b> when any attempt to display UI is detected. Set this flag only if the function will be called from a component (such as a service) that cannot display UI. 

<div class="alert"><b>Note</b>    If this flag is set and a UI display is attempted, the device can be left in an indeterminate state.</div>
<div> </div>

##### - InstallFlags.INSTALLFLAG_READONLY

If this flag is set, the function will not copy, rename, or delete any installation files. Use of this flag should be limited to environments in which file access is restricted or impossible, such as an "embedded" operating system.

## -returns

The function returns <b>TRUE</b> if a device was upgraded to the specified driver.

Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <b>GetLastError</b>. Possible error values returned by <b>GetLastError</b> are included in the following table.


<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The path that was specified for <i>FullInfPath</i> does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IN_WOW64</b></dt>
</dl>
</td>
<td width="60%">
The calling application is a 32-bit application attempting to execute in a 64-bit environment, which is not allowed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value specified for <i>InstallFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DEVINST</b></dt>
</dl>
</td>
<td width="60%">
The value specified for <i>HardwareId</i> does not match any device on the system. That is, the device is not plugged in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The function found a match for the <i>HardwareId</i> value, but the specified driver was not a better match than the current driver and the caller did not specify the INSTALLFLAG_FORCE flag. 

</td>
</tr>
</table>

## -remarks

<b>UpdateDriverForPlugAndPlayDevices</b> scans the devices on the system and attempts to install the drivers specified by <i>FullInfPath</i> for any devices that match the specified <i>HardwareId</i> value. 

The default behavior is to only install the specified drivers if they are better match than the currently installed drivers and the specified drivers are also a better match than any drivers in %<i>SystemRoot</i>%&#92;<i>inf</i>. For more information, see <a href="/windows-hardware/drivers/install/how-setup-selects-drivers">How Windows Selects Drivers</a>. 

<b>UpdateDriverForPlugAndPlayDevices</b> can also be used to determine whether the device with the specified <i>HardwareId</i> value is plugged in. For more information, see <a href="/windows-hardware/drivers/install/writing-a-device-installation-application">Writing a Device Installation Application</a>.

<b>UpdateDriverForPlugAndPlayDevices</b> sends an <a href="/windows-hardware/drivers/kernel/irp-mn-query-remove-device">IRP_MN_QUERY_REMOVE_DEVICE</a> request to the specified device, all the children of the device, and all other devices that are recursively part of the removal relations for the device. If any of these devices fail a query remove request, <b>UpdateDriverForPlugAndPlayDevices</b> sets the DI_NEEDREBOOT flag in the <b>Flags</b> member of the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure for the device. For information about removal relations, see the <a href="/windows-hardware/drivers/kernel/irp-mn-query-device-relations">IRP_MN_QUERY_DEVICE_RELATIONS</a> request.

Generally, <a href="/windows-hardware/drivers/">device installation applications</a> should supply <b>NULL</b> for <i>bRebootRequired</i>. So, the system will initiate a restart if necessary. An application should specify a pointer value <i>only</i> in the following cases:

<ul>
<li>
The application must call <b>UpdateDriverForPlugAndPlayDevices</b> several times to complete an installation. 

</li>
<li>
The application must perform other operations before the restart (if required) occurs.

</li>
<li>
The application is a class installer, which should set DI_NEEDREBOOT in <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> if a restart is needed.

</li>
</ul>
If the application must call <b>UpdateDriverForPlugAndPlayDevices</b> several times, it should save any <b>TRUE</b> restart status value received and then prompt for a restart after the final call has returned.

If the function returns ERROR_IN_WOW64 in a 32-bit application, the application is executing on a 64-bit system, which is not allowed. For more information, see <a href="/windows-hardware/drivers/install/device-installations-on-64-bit-systems">Installing Devices on 64-Bit Systems</a>.
