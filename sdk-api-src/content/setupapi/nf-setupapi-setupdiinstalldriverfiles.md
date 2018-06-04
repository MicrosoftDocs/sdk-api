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

# SetupDiInstallDriverFiles function


## -description


The <b>SetupDiInstallDriverFiles</b> function is the default handler for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543694">DIF_INSTALLDEVICEFILES</a> installation request. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains the device information element that represents the device for which to install files. The device information set must not contain remote elements.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of <b>SetupDiInstallDriverFiles</b> must be a member of the Administrators group if this function is being used to install files. However, if this function is being used to build up a file queue, membership in the Administrators group is not required.

<div class="alert"><b>Note</b>  Only a class installer should call <b>SetupDiInstallDriverFiles</b> and only in those situations where the class installer must perform driver file installation operations after <b>SetupDiInstallDriverFiles</b> completes the default driver file installation operation. In such situations, the class installer must directly call <b>SetupDiInstallDriverFiles</b> when the installer processes a DIF_INSTALLDEVICEFILES request. For more information about calling the default handler, see <a href="devinst.calling_the_default_dif_code_handlers">Calling Default DIF Code Handlers</a>.</div>
<div> </div>
The operation of <b>SetupDiInstallDriverFiles</b> is similar to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff552039">SetupDiInstallDevice</a> function. However, this function performs only the file copy operations that are performed by <b>SetupDiInstallDevice</b>. 

A driver must be selected for the specified device information set or element before this function is called.

This function processes the <b>CopyFiles</b>, <b>Delfiles</b>, and <b>Renfiles</b> entries in the selected INF file.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550922">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552039">SetupDiInstallDevice</a>
 

 

