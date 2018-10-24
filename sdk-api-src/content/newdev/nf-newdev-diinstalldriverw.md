---
UID: NF:newdev.DiInstallDriverW
title: DiInstallDriverW function
author: windows-sdk-content
description: The DiInstallDriver function preinstalls a driver in the driver store and then installs the driver on devices present in the system that the driver supports.
old-location: devinst\diinstalldriver.htm
tech.root: devinst
ms.assetid: 7015d05f-235e-42d1-b4e1-9919bbebf185
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DiInstallDriver, DiInstallDriver function [Device and Driver Installation], DiInstallDriverA, DiInstallDriverW, devinst.diinstalldriver, di-rtns_acf16c10-0aba-472a-8e3d-9c7dcc136449.xml, newdev/DiInstallDriver
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Newdev.lib
 - Newdev.dll
api_name:
 - DiInstallDriver
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DiInstallDriverW function


## -description


The <b>DiInstallDriver</b> function preinstalls a driver in the <a href="devinst.driver_store">driver store</a> and then installs the driver on devices present in the system that the driver supports.


## -parameters




### -param hwndParent [in, optional]

A handle to the top-level window that <b>DiInstallDriver</b> uses to display any user interface component that is associated with installing the device. This parameter is optional and can be set to <b>NULL</b>. 


### -param InfPath [in]

A pointer to a NULL-terminated string that supplies the fully qualified path of the INF file for the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a>.


### -param Flags [in]

A value of type DWORD that specifies zero or DIIRFLAG_FORCE_INF. Typically, this flag should be set to zero. 

If this flag is zero, <b>DiInstallDriver</b> only installs the specified driver on a device if the driver is a better match for a device than the driver that is currently installed on a device. However, if this flag is set to DIIRFLAG_FORCE_INF, <b>DiInstallDriver</b> installs the specified driver on a matching device whether the driver is a better match for the device than the driver that is currently installed on the device. 

<div class="alert"><b>Caution</b>  Forcing the installation of the driver can result in replacing a more compatible or newer driver with a less compatible or older driver. </div>
<div> </div>
For information about how Windows selects a driver for a device, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/how-setup-selects-drivers">How Windows Selects Drivers</a>.


### -param NeedReboot [out, optional]

A pointer to a value of type BOOL that <b>DiInstallDriver</b> sets to indicate whether a system is restart is required to complete the installation. This parameter is optional and can be <b>NULL</b>. If the parameter is supplied and a system restart is required to complete the installation, <b>DiInstallDriver</b> sets the value to <b>TRUE</b>. In this case, the caller must prompt the user to restart the system. If this parameter is supplied and a system restart is not required to complete the installation, <b>DiInstallDriver</b> sets the value to <b>FALSE</b>. If the parameter is <b>NULL</b> and a system restart is required to complete the installation, <b>DiInstallDriver</b> displays a system restart dialog box. For more information about this parameter, see the following <b>Remarks</b> section. 


## -returns



<b>DiInstallDriver</b> returns <b>TRUE</b> if the function successfully preinstalled the specified <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> in the <a href="devinst.driver_store">driver store</a>. <b>DiInstallDriver</b> also returns <b>TRUE</b> if the function successfully installed the driver on one or more devices in the system. If the driver package is not successfully installed in the driver store, <b>DiInstallDriver</b> returns <b>FALSE</b> and the logged error can be retrieved by making call to <b>GetLastError</b>. Some of the more common error values that <b>GetLastError</b> might return are as follows:

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
The caller does not have Administrator privileges. By default, Windows requires that the caller have Administrator privileges to preinstall a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> in the <a href="devinst.driver_store">driver store</a>. 

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
The value specified for <i>Flags</i> is not equal to zero or DIIRFLAG_FORCE_INF.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IN_WOW64</b></dt>
</dl>
</td>
<td width="60%">
The calling application is a 32-bit application that is attempting to execute in a 64-bit environment, which is not allowed. For more information, see <a href="devinst.device_installations_on_64_bit_systems">Installing Devices on 64-Bit Systems</a>.

</td>
</tr>
</table>
 




## -remarks



<b>DiInstallDriver</b> performs the following operations:

<ol>
<li>
Preinstalls the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> in the <a href="devinst.driver_store">driver store</a>. If there is an instance of the same driver package already preinstalled in the driver store, <b>DiInstallDriver</b> first removes that instance and then adds the new instance of the driver package to the driver store. 

</li>
<li>
Enumerates devices that are present in the system.

</li>
<li>
If <i>Flags</i> is equal to zero, installs the driver on a device only if the specified driver is a better match for the device than the driver that is currently installed on the device. 

</li>
<li>
If <i>Flags</i> is equal to DIIRFLAG_FORCE_INF, installs the driver on a device regardless of whether the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff544817">driver package</a> is the better match to the device than the driver that is currently installed on the device. 

</li>
</ol>
In general, an installation application should set <i>NeedReboot</i> to <b>NULL</b> to direct <b>DiInstallDriver</b> to prompt the user to restart the system if a restart is required to complete the installation. An application should supply a <i>NeedReboot</i> pointer only in the following cases:

<ul>
<li>
The application must call <b>DiInstallDriver</b> several times to complete an installation. In this case, the application should record whether a <b>TRUE</b><i>NeedReboot</i> value is returned by any of the calls to <b>DiInstallDriver</b> and, if so, prompt the user to restart the system after the final call to <b>DiInstallDriver</b> returns.

</li>
<li>
The application must perform required operations, other than calling <b>DiInstallDriver</b>, before a system restart should occur. If a system restart is required, the application should finish the required operations and then prompt the user to restart the system. 

</li>
<li>
The application is a class installer, in which case, the class installer should set the DI_NEEDREBOOT flag in the <b>Flags</b> member of the SP_DEVINSTALL_PARAMS structure for a device.

</li>
</ul>
To install a selected driver on a selected device, call <a href="https://msdn.microsoft.com/e107fc37-02cb-4d50-822c-1c6fd80d7532">DiInstallDevice</a>. For more info, see <a href="devinst.setupapi_functions_that_simplify_driver_installation">SetupAPI Functions that Simplify Driver Installation</a>.




## -see-also




<a href="https://msdn.microsoft.com/e107fc37-02cb-4d50-822c-1c6fd80d7532">DiInstallDevice</a>
 

 

