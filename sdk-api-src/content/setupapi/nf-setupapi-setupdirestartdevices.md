---
UID: NF:setupapi.SetupDiRestartDevices
title: SetupDiRestartDevices function (setupapi.h)
description: The SetupDiRestartDevices function restarts a specified device or, if necessary, restarts all devices that are operated by the same function and filter drivers that operate the specified device.
helpviewer_keywords: ["SetupDiRestartDevices","SetupDiRestartDevices function [Device and Driver Installation]","devinst.setupdirestartdevices","di-rtns_9e27f3b7-c33c-44f1-b804-521d7403ac4f.xml","setupapi/SetupDiRestartDevices"]
old-location: devinst\setupdirestartdevices.htm
tech.root: devinst
ms.assetid: 38bb2e40-e522-4155-9d2c-f6aaeea70839
ms.date: 12/05/2018
ms.keywords: SetupDiRestartDevices, SetupDiRestartDevices function [Device and Driver Installation], devinst.setupdirestartdevices, di-rtns_9e27f3b7-c33c-44f1-b804-521d7403ac4f.xml, setupapi/SetupDiRestartDevices
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Server 2003 and later versions of Windows.
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
 - SetupDiRestartDevices
 - setupapi/SetupDiRestartDevices
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
 - SetupDiRestartDevices
---

# SetupDiRestartDevices function


## -description

The <b>SetupDiRestartDevices</b> function restarts a specified device or, if necessary, restarts all devices that are operated by the same function and filter drivers that operate the specified device.

## -parameters

### -param DeviceInfoSet [in]

A handle to a <a href="/windows-hardware/drivers/install/device-information-sets">device information set</a> that contains the device information element that represents the device to restart.

### -param DeviceInfoData [in, out]

A pointer to an <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a> structure for the device information member that represents the device to restart. This parameter is also an output parameter because <b>SetupDiRestartDevices</b> updates the device installation parameters for this device information member and the status and problem code of the corresponding device instance. For more information about these updates, see the following <b>Remarks</b> section.

## -returns

If the operation succeeds, <b>SetupDiRestartDevices</b> returns <b>TRUE</b>; otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetupDiRestartDevices</b> should be called only by a class installer when a class installer is handling a DIF_INSTALLDEVICE request and only in rare situations where the class installer must perform operations after all default installation operations, except for starting a device, have completed . For more information about calling <b>SetupDiRestartDevices</b> in these situations, see <a href="/windows-hardware/drivers/install/dif-installdevice">DIF_INSTALLDEVICE</a>.

<b>SetupDiRestartDevices</b> restarts only the specified device if the restart can be performed without affecting the installation of other devices that are operated by the same function driver or filter drivers that operate the device. Specifically, if the restart of the specified device does not copy new files or modify any files that were previously installed for the device, <b>SetupDiRestartDevices</b> restarts only the specified device. Otherwise, the function restarts all devices that are operated by the same function and filter drivers that operate the specified device. 

<b>SetupDiRestartDevices</b> updates the device installation parameters and device status to reflect the result of the attempted restart operation. For example:

<ul>
<li>
If the device is started, <b>SetupDiRestartDevices</b> sets the device status to DN_STARTED. 

</li>
<li>
If a system restart is necessary to start a device, <b>SetupDiRestartDevices</b> sets the DI_NEEDREBOOT flag in the <b>Flags</b> member of the SP_DEVINSTALL_PARAMETER structure that is associated with the device information element and sets the problem code for the device to CM_PROB_NEED_RESTART. 

</li>
</ul>
The <a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status">CM_Get_DevNode_Status</a> function retrieves the status and problem code for a device instance and the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a> function retrieves the device installation parameters for the device information element that represents the device instance.

## -see-also

<a href="/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_devnode_status">CM_Get_DevNode_Status</a>



<a href="/windows-hardware/drivers/install/dif-installdevice">DIF_INSTALLDEVICE</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_devinfo_data">SP_DEVINFO_DATA</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstallparamsa">SetupDiGetDeviceInstallParams</a>