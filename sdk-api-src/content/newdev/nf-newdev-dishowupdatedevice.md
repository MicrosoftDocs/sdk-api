---
UID: NF:newdev.DiShowUpdateDevice
title: DiShowUpdateDevice function (newdev.h)
description: The DiShowUpdateDevice function displays the Hardware Update wizard for a specified device.
helpviewer_keywords: ["DiShowUpdateDevice","DiShowUpdateDevice function [Device and Driver Installation]","devinst.dishowupdatedevice","di-rtns_096f087c-2947-4424-861d-af7287eec8ad.xml","newdev/DiShowUpdateDevice"]
old-location: devinst\dishowupdatedevice.htm
tech.root: devinst
ms.assetid: 4b60f7cd-0375-4569-abb1-721fd8cdf5a1
ms.date: 12/05/2018
ms.keywords: DiShowUpdateDevice, DiShowUpdateDevice function [Device and Driver Installation], devinst.dishowupdatedevice, di-rtns_096f087c-2947-4424-861d-af7287eec8ad.xml, newdev/DiShowUpdateDevice
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
 - DiShowUpdateDevice
 - newdev/DiShowUpdateDevice
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
 - DiShowUpdateDevice
---

# DiShowUpdateDevice function


## -description

The <b>DiShowUpdateDevice</b> function displays the Hardware Update wizard for a specified device.

## -parameters

### -param hwndParent [in, optional]

A handle to the top-level window that <b>DiShowUpdateDevice</b> uses to display any user interface components that are associated with updating the specified device. This parameter is optional and can be set to <b>NULL</b>.

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element that represents the device for which to show the Hardware Update wizard.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the device for which to show the Hardware Update wizard.

### -param Flags [in]

This parameter must be set to zero.

### -param NeedReboot [out, optional]

A pointer to a value of type BOOL that <b>DiShowUpdateDevice</b> sets to indicate whether a system restart is required to complete the driver update. This parameter is optional and can be <b>NULL</b>. If the parameter is supplied and a system restart is required to complete the driver update, <b>DiShowUpdateDevice</b> sets the value to <b>TRUE</b>. In this case, the caller must prompt the user to restart the system. If this parameter is supplied and a system restart is not required to complete the installation, <b>DiShowUpdateDevice</b> sets the value to <b>FALSE</b>. If the parameter is <b>NULL</b> and a system restart is required to complete the driver update, <b>DiShowUpdateDevice</b> displays a system restart dialog box. For more information about this parameter, see the following <b>Remarks</b> section.

## -returns

<b>DiShowUpdateDevice</b> returns <b>TRUE</b> if the Hardware Update wizard successfully updated the driver for the specified device. Otherwise, <b>DiShowUpdateDevice</b> returns <b>FALSE</b> and the logged error can be retrieved by making a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some of the more common error values that <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> might return are as follows:

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
The caller does not have Administrator privileges. By default, Windows requires that the calling process have Administrator privileges to update a <a href="/previous-versions/windows/hardware/difxapi/driverpackagepreinstall">driver package</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANCELLED</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the Hardware Update wizard.

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
The value specified for <i>Flags</i> is not equal to zero.

</td>
</tr>
</table>

## -remarks

<b>DiShowUpdateDevice</b> displays the Hardware Update wizard for the specified device instance. For information about how to update device drivers by using the Hardware Update wizard, see Help and Support Center.

In general, installation applications should set <i>NeedReboot</i> to <b>NULL</b> so that the system will automatically initiate a system restart if a restart is required to complete a hardware update. An application should supply a <i>NeedReboot</i> pointer only in the following cases:

<ul>
<li>
The installation application must call <b>DiShowUpdateDevice</b> several times to complete hardware updates. In this case, the application should record whether a <b>TRUE</b><i>NeedReboot</i> value is returned by any of the calls to <b>DiShowUpdateDevice</b> and, if so, prompt the user to restart the system after the final call to <b>DiShowUpdateDevice</b> returns.

</li>
<li>
The application must perform required operations, other than calling <b>DiShowUpdateDevice</b>, before a system restart should occur. If a system restart is required, the application should finish the required operations and then prompt the user to restart the system.

</li>
</ul>
To roll back a driver for a device instead of invoking the Hardware Update wizard, call <a href="/windows/desktop/api/newdev/nf-newdev-dirollbackdriver">DiRollbackDriver</a>.

To install a new driver for a device instead of invoking the Hardware Update wizard, call <a href="/windows/desktop/api/newdev/nf-newdev-diinstalldrivera">DiInstallDriver</a> or <a href="/windows/desktop/api/newdev/nf-newdev-updatedriverforplugandplaydevicesa">UpdateDriverForPlugAndPlayDevices</a>.

## -see-also

<a href="/windows/desktop/api/newdev/nf-newdev-diinstalldrivera">DiInstallDriver</a>



<a href="/windows/desktop/api/newdev/nf-newdev-dirollbackdriver">DiRollbackDriver</a>



<a href="/windows/desktop/api/newdev/nf-newdev-updatedriverforplugandplaydevicesa">UpdateDriverForPlugAndPlayDevices</a>