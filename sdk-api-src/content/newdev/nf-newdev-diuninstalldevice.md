---
UID: NF:newdev.DiUninstallDevice
title: DiUninstallDevice function (newdev.h)
description: The DiUninstallDevice function uninstalls a device and removes its device node (devnode) from the system.
helpviewer_keywords: ["DiUninstallDevice","DiUninstallDevice function [Device and Driver Installation]","devinst.diuninstalldevice","di-rtns_361ca427-6e65-497e-a9c0-8723e4aaa8c6.xml","newdev/DiUninstallDevice"]
old-location: devinst\diuninstalldevice.htm
tech.root: devinst
ms.assetid: 317b24bd-01a8-41ff-9aac-78690574eade
ms.date: 12/05/2018
ms.keywords: DiUninstallDevice, DiUninstallDevice function [Device and Driver Installation], devinst.diuninstalldevice, di-rtns_361ca427-6e65-497e-a9c0-8723e4aaa8c6.xml, newdev/DiUninstallDevice
req.header: newdev.h
req.include-header: Newdev.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
 - DiUninstallDevice
 - newdev/DiUninstallDevice
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
 - Ext-MS-Win-NewDev-Config-l1-1-0.dll
 - Ext-MS-Win-Newdev-Config-L1-1-1.dll
api_name:
 - DiUninstallDevice
---

# DiUninstallDevice function


## -description

The <b>DiUninstallDevice</b> function uninstalls a device and removes its device node (<a href="/windows-hardware/drivers/">devnode</a>) from the system. This differs from using <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a> with the <a href="/windows-hardware/drivers/install/dif-remove">DIF_REMOVE</a> code because it attempts to uninstall the device node in addition to child devnodes that are present at the time of the call.

Prior to Windows 8 any child devices that are not present at the time of the call will not be uninstalled.  However, beginning with Windows 8, any child devices that are not present at the time of the call will be uninstalled.

## -parameters

### -param hwndParent [in]

A handle to the top-level window that is used to display any user interface component that is associated with the uninstallation request for the device. This parameter is optional and can be set to <b>NULL</b>.

### -param DeviceInfoSet [in]

A handle to the <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains a device information element. This element represents the device to be uninstalled through this call.

### -param DeviceInfoData [in]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the specified device in the specified device information set for which the uninstallation request is performed.

### -param Flags [in]

A value of type DWORD that specifies device uninstallation flags. Starting with Windows 7, this parameter must be set to zero.

### -param NeedReboot [out, optional]

A pointer to a value of type BOOL that <b>DiUninstallDevice</b> sets to indicate whether a system restart is required to complete the device uninstallation request. This parameter is optional and can be set to <b>NULL</b>.

If the parameter is given and a system restart is required, <b>DiUninstallDevice</b> sets the value to <b>TRUE</b>. In this case, the application must prompt the user to restart the system. If this parameter is supplied and a system restart is not required, <b>DiUninstallDevice</b> sets the value to <b>FALSE</b>. 

If this parameter is <b>NULL</b> and a system restart is required to complete the device uninstallation, <b>DiUninstallDevice</b> displays a system restart dialog box.

For more information about this parameter, see the <b>Remarks</b> section.

## -returns

<b>DiUninstallDevice</b> returns <b>TRUE</b> if the function successfully uninstalled the top-level device node that represents the device.  Otherwise, <b>DiUninstallDevice</b> returns <b>FALSE</b>, and the logged error can be retrieved by making a call to <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list shows some of the more common error values that <b>GetLastError</b> might return for this API:

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
The caller does not have Administrator privileges. By default, Windows requires that the caller have Administrator privileges to uninstall devices.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The value that is specified for the <i>Flags</i> parameter is not equal to zero.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  The return value does not indicate that the removal of all child devnodes has succeeded or failed. Starting with Windows Vista, information about the status of the removal of child devnodes  is available in the <i>Setupapi.dev.log</i> file. For more information about this file, see <a href="/windows-hardware/drivers/install/setupapi-text-logs">SetupAPI Text Logs</a>.</div>
<div> </div>

## -remarks

<b>DiUninstallDevice</b> performs the same function as <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a> when used with the <a href="/windows-hardware/drivers/install/dif-remove">DIF_REMOVE</a> code. The key difference is that child devnodes for the top-level device are also deleted. <b>DiUninstallDevice</b> only returns failure if the top-level device node failed to be uninstalled, which is consistent with the behavior of <b>SetupDiCallClassInstaller</b> when used with the <b>DIF_REMOVE</b> code. Detailed information about whether child devnode uninstallation succeeded is available in the Setupapi.dev.log file.

The device to be uninstalled is specified by providing a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that includes the referenced device, and a <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure for the specific device. These are provided in the <i>DeviceInfoSet</i> and <i>DeviceInfoData</i> parameters.

To create a device information set that contains the specified device and to obtain an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure for the device, complete one of the following tasks:

<ul>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a> to retrieve a device information set that contains the device and then call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a> to enumerate the devices in the device information set. On each call, <b>SetupDiEnumDeviceInfo</b> returns an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the enumerated device in the device information set. 

To obtain specific information about the enumerated device, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a> and supply the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that is returned by <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a>.

</li>
<li>
Call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a> to add a device with a known device instance ID to the device information set. <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiopendeviceinfoa">SetupDiOpenDeviceInfo</a> returns an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure that represents the device in the device information set. 

</li>
</ul>
In case the device uninstallation request requires a restart of the computer, <b>DiUninstallDevice</b> prompts the user to restart the system if the <i>NeedReboot</i> parameter is set to <b>NULL</b>. If there is any user interface window that the application is using, the <i>hwndParent</i> parameter should be set to the value of that window's handle. 

However, if the application manages the notification of a required system restart, it must set the <i>NeedReboot</i> parameter to a non-<b>NULL</b> value. <b>DiUninstallDevice</b> sets the <i>NeedReboot</i> parameter to <b>TRUE</b> or <b>FALSE</b>, depending on whether a system restart is required. 

The following list shows examples of why the application might manage the system restart:

<ul>
<li>
The application has to uninstall several devices. After all the devices are uninstalled, the application should prompt the user to restart the system if any call to <b>DiUninstallDevice</b> returned <b>TRUE</b> in the <i>NeedReboot</i> parameter.

</li>
<li>
The application requires some other operations to occur before the system can be restarted. If a system restart is required, the application should finish the required operations and then prompt the user to restart the system.

</li>
<li>
The application is a class installer. In this case, the class installer should set the <b>DI_NEEDREBOOT</b> flag in the <b>Flags</b> member of the <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a> structure for a device. 

</li>
</ul>

## -see-also

<a href="/windows-hardware/drivers/install/dif-remove">DIF_REMOVE</a>



<a href="/windows-hardware/drivers/install/device-information-sets">Device information set</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinstall_params_a">SP_DEVINSTALL_PARAMS</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdeviceinfo">SetupDiEnumDeviceInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetclassdevsw">SetupDiGetClassDevs</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdevicepropertyw">SetupDiGetDeviceProperty</a>