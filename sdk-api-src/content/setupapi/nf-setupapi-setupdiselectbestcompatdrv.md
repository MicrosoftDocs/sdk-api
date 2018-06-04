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

# SetupDiSelectBestCompatDrv function


## -description


The <b>SetupDiSelectBestCompatDrv</b> function is the default handler for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543719">DIF_SELECTBESTCOMPATDRV</a> installation request.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to select the best compatible driver.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. <b>SetupDiSelectBestCompatDrv</b> selects the best driver for a device information element from the compatible driver list for the specified device. 


## -returns



If the operation succeeds, <b>SetupDiSelectBestCompatDrv</b> returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the caller of <b>SetupDiSelectBestCompatDrv</b> is a member of the Administrators group and the class of the device is different that the class of the selected driver, <b>SetupDiSelectBestCompatDrv</b> sets the class of the device to the class of the driver. If this behavior is not desired, call this function at a lower privilege level. 

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiSelectBestCompatDrv</b> and only in those situations where the class installer must perform driver selection operations after <b>SetupDiSelectBestCompatDrv</b> completes the default driver selection operation. In such situations, the class installer must directly call <b>SetupDiSelectBestCompatDrv</b> when the installer processes a DIF_SELECTBESTCOMPATDRV request. For more information about calling the default handler, see <a href="devinst.calling_the_default_dif_code_handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
<b>SetupDiSelectBestCompatDrv </b>is primarily designed to select the best compatible driver for a device information element on a local computer. Although <b>SetupDiSelectBestCompatDrv </b>will not fail if the device information set is for a remote computer, the result is of limited use because the device information set cannot subsequently be used as input with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations for a remote computer. In particular, the device information set cannot subsequently be used as input with a DIF_INSTALLDEVICE installation request to install a device on a remote computer.

For information about how the best driver is selected, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/how-setup-selects-drivers">How Windows Selects Drivers</a>.

To get the selected driver for a device, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff552013">SetupDiGetSelectedDriver</a>. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff543719">DIF_SELECTBESTCOMPATDRV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a>
 

 

