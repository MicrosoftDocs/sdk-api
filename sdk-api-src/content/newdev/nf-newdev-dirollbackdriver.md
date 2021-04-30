---
UID: NF:newdev.DiRollbackDriver
title: DiRollbackDriver function (newdev.h)
description: The DiRollbackDriver function rolls back the driver that is installed on a specified device.
helpviewer_keywords: ["DiRollbackDriver","DiRollbackDriver function [Device and Driver Installation]","devinst.dirollbackdriver","di-rtns_982c291b-0aad-475c-ba3a-0e08ab0f584a.xml","newdev/DiRollbackDriver"]
old-location: devinst\dirollbackdriver.htm
tech.root: devinst
ms.assetid: 12296991-cbf9-421e-a16e-ca8a22fc29a1
ms.date: 12/05/2018
ms.keywords: DiRollbackDriver, DiRollbackDriver function [Device and Driver Installation], devinst.dirollbackdriver, di-rtns_982c291b-0aad-475c-ba3a-0e08ab0f584a.xml, newdev/DiRollbackDriver
req.header: newdev.h
req.include-header: Newdev.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
 - DiRollbackDriver
 - newdev/DiRollbackDriver
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Newdev.dll
api_name:
 - DiRollbackDriver
---

# DiRollbackDriver function


## -description

The <b>DiRollbackDriver</b> function rolls back the driver that is installed on a specified device.

## -parameters

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which driver rollback is performed.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the specific device in the specified device information set for which driver rollback is performed.

### -param hwndParent [in, optional]

A handle to the top-level window that <b>DiRollbackDriver</b> uses to display any user interface component that is associated with a driver rollback for the specified device. This parameter is optional and can be set to <b>NULL</b>.

### -param Flags [in]

A value of type DWORD that can be set to zero or ROLLBACK_FLAG_NO_UI. 

Typically, this flag should be set to zero, in which case <b>DiRollbackDriver</b> does not suppress the default user interface components that are associated with a driver rollback. However, if this flag is set to ROLLBACK_FLAG_NO_UI, <b>DiRollbackDriver</b> suppresses the display of user interface components that are associated with a driver rollback.

### -param NeedReboot [out, optional]

A pointer to a value of type BOOL that <b>DiRollbackDriver</b> sets to indicate whether a system restart is required to complete the rollback. This parameter is optional and can be <b>NULL</b>. 

If the parameter is supplied and a system restart is required to complete the rollback, <b>DiRollbackDriver</b> sets the value to <b>TRUE</b>. In this case, the caller must prompt the user to restart the system. If this parameter is supplied and a system restart is not required to complete the installation, <b>DiRollbackDriver</b> sets the value to <b>FALSE</b>. 

If the parameter is <b>NULL</b> and a system restart is required to complete the rollback, <b>DiRollbackDriver</b> displays a system restart dialog box. 

For more information about this parameter, see the following <b>Remarks</b> section.

## -returns

<b>DiRollbackDriver</b> returns <b>TRUE</b> if the function successfully rolled back the driver for the device; otherwise, <b>DiRollbackDriver</b> returns <b>FALSE</b> and the logged error can be retrieved by making a call to <b>GetLastError</b>. Some of the more common error values that <b>GetLastError</b> might return are as follows:

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
The caller does not have Administrator privileges. By default, Windows requires that the caller have Administrator privileges to roll back a <a href="/previous-versions/windows/hardware/difxapi/driverpackagepreinstall">driver package</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value specified for <i>Flags</i> is not equal to zero or ROLLBACK_FLAG_NO_UI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
A backup driver is not set for the device.

</td>
</tr>
</table>

## -remarks

If a previously installed backup driver is set for a device, a driver rollback for the device replaces the driver that is currently installed on the device with the backup driver. Windows maintains at most one backup driver for a device. Windows sets a driver as the backup driver for a device immediately after the driver is successfully installed on the device and Windows determines that the device is functioning correctly. However, if a driver does not install successfully on a device or the device does not function correctly after the installation, Windows does not set the driver as the backup driver for the device. For more information about driver rollback, see information about Device Manager in Help and Support Center.

If the specified device has a backup driver, <b>DiRollbackDriver</b> performs the following operations:

<ol>
<li>
If <i>Flags</i> is set to zero, <b>DiRollbackDriver</b> prompts the user to confirm whether the backup driver should be installed. Otherwise, if <i>Flags</i> is set to ROLLBACK_FLAG_NO_UI, <b>DiRollbackDriver</b> installs the backup driver without prompting the user to confirm the installation of the backup driver.

</li>
<li>
<b>DiRollbackDriver</b> installs the backup driver. The driver is installed whether the backup driver is a better match for the device than the driver that is currently installed on the device.

</li>
<li>
If the driver that is replaced by the backup driver is not an inbox driver and is not installed on any other devices in the system, <b>DiRollbackDriver</b> removes the driver from the system. <b>DiRollbackDriver</b> removes the driver from the system because it is assumed that a user will replace a driver only if there is a problem with the driver. 

</li>
</ol>
If the specified device does not have a backup driver, <b>DiRollbackDriver</b> calls <b>SetLastError</b> to set the error ERROR_NO_MORE_ITEMS, does not remove the currently installed driver, and returns <b>FALSE</b>.

In general, installation applications should set <i>NeedReboot</i> to <b>NULL</b> so that the system will automatically initiate a system restart if a restart is required to complete the rollback. An application should supply a <i>NeedReboot</i> pointer only in the following cases:

<ul>
<li>
The application must call <b>DiRollbackDriver</b> several times to complete an installation. In this case, the application should record whether a <b>TRUE</b><i>NeedReboot</i> value is returned by any of the calls to <b>DiRollbackDriver</b> and, if so, prompt the user to restart the system after the final call to <b>DiRollbackDriver</b> returns.

</li>
<li>
The application must perform required operations, other than calling <b>DiRollbackDriver</b>, before a system restart should occur. If a system restart is required, the application should finish the required operations and then prompt the user to restart the system. 

</li>
</ul>
To install a new driver for a device instead of rolling back the driver for the device, call <a href="/windows/desktop/api/newdev/nf-newdev-diinstalldrivera">DiInstallDriver</a> or <a href="/windows/desktop/api/newdev/nf-newdev-updatedriverforplugandplaydevicesa">UpdateDriverForPlugAndPlayDevices</a>.

## -see-also

<a href="/windows/desktop/api/newdev/nf-newdev-diinstalldrivera">DiInstallDriver</a>



<a href="/windows/desktop/api/newdev/nf-newdev-updatedriverforplugandplaydevicesa">UpdateDriverForPlugAndPlayDevices</a>