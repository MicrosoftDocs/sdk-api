---
UID: NF:newdev.DiUninstallDriverW
title: DiUninstallDriverW function (newdev.h)
description: The DiUninstallDriver function removes a driver package from any devices it is installed on by installing those devices with another matching driver package, if available, or the null driver if no other matching driver package is available. Then the specified driver package is removed from the driver store. (Unicode)
helpviewer_keywords: ["DiUninstallDriver", "DiUninstallDriver function [Device and Driver Installation]", "DiUninstallDriverW", "devinst.diuninstalldriver", "di-rtns_acf16c10-0aba-472a-8e3d-9c7dcc136449.xml", "newdev/DiUninstallDriver"]
old-location: devinst\diuninstalldriver.htm
tech.root: devinst
ms.assetid: 7015d05f-235e-42d1-b4e1-9919bbebf185
ms.date: 12/05/2018
ms.keywords: DiUninstallDriver, DiUninstallDriver function [Device and Driver Installation], DiUninstallDriverA, DiUninstallDriverW, devinst.diuninstalldriver, di-rtns_acf16c10-0aba-472a-8e3d-9c7dcc136449.xml, newdev/DiUninstallDriver
req.header: newdev.h
req.include-header: Newdev.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 10 Version 1703 and later versions of Windows.
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
 - DiUninstallDriverW
 - newdev/DiUninstallDriverW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - ext-ms-win-newdev-config-l1-1-2.dll
 - Newdev.lib
 - Newdev.dll
api_name:
 - DiInstallDriver
 - diuninstalldriverw
---

# DiUninstallDriverW function


## -description

The <b>DiUninstallDriver</b> function removes a driver package from any devices it is installed on by installing those devices with another matching driver package, if available, or the null driver if no other matching driver package is available. Then the specified driver package is removed from the <a href="/windows-hardware/drivers/install/driver-store">driver store.</a> 

## -parameters

### -param hwndParent [in, optional]

A handle to the top-level window that <b>DiUninstallDriver</b> should use to display any user interface component that is associated with uninstalling the driver. This parameter is optional and can be set to <b>NULL</b>.

### -param InfPath [in]

A pointer to a NULL-terminated string that supplies the fully qualified path of the INF file for the <a href="/windows-hardware/drivers/install/driver-packages">driver package</a>.

### -param Flags [in]

A value of type DWORD that specifies zero or one or more of the following flags: DIURFLAG_NO_REMOVE_INF. Typically, this flag should be set to zero. 

If this flag is zero, <b>DiUninstallDriver</b> removes the driver package from any devices it is installed on by installing those devices with another matching driver package, if available, or the null driver if no other matching driver package is available. However, if this flag is set to DIURFLAG_NO_REMOVE_INF, <b>DiUninstallDriver</b> removes the driver package from any devices it is installed on, but does not remove the driver package from the Driver Store.

<div class="alert"><b>Caution:</b>  Forcing the uninstallation of the driver package can result in replacing a more compatible or newer driver package with a less compatible or older driver. </div>
<div> </div>
For information about how Windows selects a driver package for a device, see <a href="/windows-hardware/drivers/install/how-setup-selects-drivers">How Windows Selects Drivers</a>.

### -param NeedReboot [out, optional]

A pointer to a value of type BOOL that <b>DiUninstallDriver</b> sets to indicate whether a system restart is required to complete the uninstallation. This parameter is optional and can be <b>NULL</b>. If the parameter is supplied and a system restart is required to complete the uninstallation, <b>DiUninstallDriver</b> sets the value to <b>TRUE</b>. In this case, the caller must prompt the user to restart the system. If this parameter is supplied and a system restart is not required to complete the uninstallation, <b>DiUninstallDriver</b> sets the value to <b>FALSE</b>. If the parameter is <b>NULL</b> and a system restart is required to complete the uninstallation, <b>DiUninstallDriver</b> displays a system restart dialog box. For more information about this parameter, see the following <b>Remarks</b> section.

## -returns

<b>DiUninstallDriver</b> returns <b>TRUE</b> if the function successfully removes the <a href="/windows-hardware/drivers/install/driver-packages">driver package</a> from any devices it is installed on and is successfully removed from the driver store of the system. If the driver package is not successfully uninstalled from the driver store, <b>DiUninstallDriver</b> returns <b>FALSE</b> and the logged error can be retrieved by making a call to <b>GetLastError</b>. Some of the more common error values that <b>GetLastError</b> might return are as follows:

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
The caller does not have Administrator privileges. By default, Windows requires that the caller have Administrator privileges to uninstall a <a href="/windows-hardware/drivers/install/driver-packages">driver package</a> from the <a href="/windows-hardware/drivers/install/driver-store">driver store</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The path of the specified INF file does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value specified for <i>Flags</i> is not equal to zero or DIURFLAG_NO_REMOVE_INF.

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

In general, an uninstallation application should set <i>NeedReboot</i> to <b>NULL</b> to direct <b>DiUninstallDriver</b> to prompt the user to restart the system if a restart is required to complete the removal. An application should supply a <i>NeedReboot</i> pointer only in the following cases:

<ul>
<li>
The application must call <b>DiUninstallDriver</b> several times to complete an uninstallation. In this case, the application should record whether a <b>TRUE</b> <i>NeedReboot</i> value is returned by any of the calls to <b>DiUninstallDriver</b> and, if so, prompt the user to restart the system after the final call to <b>DiUninstallDriver</b> returns.

</li>
<li>
The application must perform required operations, other than calling <b>DiUninstallDriver</b>, before a system restart should occur. If a system restart is required, the application should finish the required operations and then prompt the user to restart the system. 

</li>

</ul>

## -see-also

<a href="/windows/desktop/api/newdev/nf-newdev-diinstalldevice">DiUninstallDevice</a>
