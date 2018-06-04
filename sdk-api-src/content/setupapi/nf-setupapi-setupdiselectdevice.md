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

# SetupDiSelectDevice function


## -description


The <b>SetupDiSelectDevice</b> function is the default handler for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543723">DIF_SELECTDEVICE</a> request.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to select a driver.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiSelectDevice</b> selects the driver for the specified device and sets <i>DeviceInfoData.</i><b>ClassGuid</b> to the GUID of the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> for the selected driver. If this parameter is <b>NULL</b>, <b>SetupDiSelectDevice</b> sets the selected driver in the global class driver list for <i>DeviceInfoSet</i>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiSelectDevice</b> handles the user interface that allows the user to select a driver for the specified device, or a device information set if a device is not specified. By setting the <b>Flags</b> field of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552346">SP_DEVINSTALL_PARAMS</a> structure for the device, or the device information set if a device is not specified, the caller can specify special handling of the user interface, for example, to allow users to select a driver from an OEM installation disk. 

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiSelectDevice</b> and only in those situations where the class installer must perform driver selection operations after <b>SetupDiSelectDevice</b> completes the default driver selection operation. In such situations, the class installer must directly call <b>SetupDiSelectDevice</b> when the installer processes a DIF_SELECTDEVICE request. For more information about calling the default handler, see <a href="devinst.calling_the_default_dif_code_handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
<b>SetupDiSelectDevice</b> is primarily designed to select a driver for a device on a local computer before installing the device. Although <b>SetupDiSelectDevice</b> will not fail if the device information set is for a remote computer, the result is of limited use because the device information set cannot subsequently be used with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations on a remote computer. In particular, the device information set cannot be used as input with a DIF_INSTALLDEVICE installation request to install a device on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552346">SP_DEVINSTALL_PARAMS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>
 

 

