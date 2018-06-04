---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# SetupDiRestartDevices function


## -description


The <b>SetupDiRestartDevices</b> function restarts a specified device or, if necessary, restarts all devices that are operated by the same function and filter drivers that operate the specified device.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_classes">device information set</a> that contains the device information element that represents the device to restart. 


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure for the device information member that represents the device to restart. This parameter is also an output parameter because <b>SetupDiRestartDevices</b> updates the device installation parameters for this device information member and the status and problem code of the corresponding device instance. For more information about these updates, see the following <b>Remarks</b> section. 


## -returns



If the operation succeeds, <b>SetupDiRestartDevices</b> returns <b>TRUE</b>; otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiRestartDevices</b> should be called only by a class installer when a class installer is handling a DIF_INSTALLDEVICE request and only in rare situations where the class installer must perform operations after all default installation operations, except for starting a device, have completed . For more information about calling <b>SetupDiRestartDevices</b> in these situations, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff543692">DIF_INSTALLDEVICE</a>.

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
The <a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a> function retrieves the status and problem code for a device instance and the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551104">SetupDiGetDeviceInstallParams</a> function retrieves the device installation parameters for the device information element that represents the device instance. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538514">CM_Get_DevNode_Status</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff543692">DIF_INSTALLDEVICE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551104">SetupDiGetDeviceInstallParams</a>
 

 

