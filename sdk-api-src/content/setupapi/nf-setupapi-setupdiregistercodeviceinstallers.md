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

# SetupDiRegisterCoDeviceInstallers function


## -description


The <b>SetupDiRegisterCoDeviceInstallers</b> function is the default handler for <a href="https://msdn.microsoft.com/library/windows/hardware/ff543715">DIF_REGISTER_COINSTALLERS</a>. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to register co-installers. The device information set must not contain any remote elements.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


## -returns



<b>SetupDiRegisterCoDeviceInstallers</b> returns <b>TRUE</b> if the function succeeds. If the function returns <b>FALSE</b>, call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> for extended error information.




## -remarks



The caller of <b>SetupDiRegisterCoDeviceInstallers</b> must be a member of the Administrators group.

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiRegisterCoDeviceInstallers</b> and only in those situations where the class installer must perform co-installer registration operations after <b>SetupDiRegisterCoDeviceInstallers</b> completes the default co-installer registration operation. In such situations, the class installer must directly call <b>SetupDiRegisterCoDeviceInstallers</b> when the installer processes a DIF_REGISTER_COINSTALLERS request. For more information about calling the default handler, see <a href="devinst.calling_the_default_dif_code_handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
<b>SetupDiRegisterCoDeviceInstallers</b> reads the INF file for the device specified by <i>DeviceInfoData</i> and creates registry entries to register any device-specific co-installers listed in the INF file. Co-installers are listed in an <a href="devinst.inf_ddinstall_coinstallers_section">INF DDInstall.CoInstallers section</a>. This function also copies the files for the co-installers, unless the DI_NOFILECOPY flag is set. 

If there is no driver selected, or the device has an INF file for Windows 9x or Millennium Edition, this function does not register any co-installers.

Registering a new device-specific co-installer invalidates the Device Installer's current list of co-installers. After a successful registration, the Device Installer updates its list of co-installers.

This function only registers device-specific co-installers, not class co-installers. 

For more information about how to write and register device-specific co-installers, see <a href="devinst.writing_a_co_installer">Writing a Co-installer</a>.

The device information set specified by <i>DeviceInfoSet</i> must only contain elements on the local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543715">DIF_REGISTER_COINSTALLERS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>
 

 

