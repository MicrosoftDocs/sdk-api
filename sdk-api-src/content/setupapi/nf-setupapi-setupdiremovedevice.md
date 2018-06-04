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

# SetupDiRemoveDevice function


## -description


The <b>SetupDiRemoveDevice</b> function is the default handler for the <a href="https://msdn.microsoft.com/library/windows/hardware/ff543717">DIF_REMOVE</a> installation request. 


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> for the local system that contains a device information element that represents the device to remove.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This is an IN-OUT parameter because <i>DeviceInfoSet</i>.<b>DevInst</b> might be updated with a new handle value upon return. If this is a global removal or the last hardware profile-specific removal, all traces of the device instance are deleted from the registry and the handle will be <b>NULL</b>. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <b>GetLastError</b>.




## -remarks



<b>SetupDiRemoveDevice</b> removes the device from the system. It deletes the device's hardware and software registry keys and any hardware-profile-specific registry keys (configuration-specific registry keys). This function dynamically stops the device if its <b>DevInst</b> is active and this is a global removal or the last configuration-specific removal. If the device cannot be dynamically stopped, flags are set in the Install Parameter block of the device information set that eventually cause the user to be prompted to restart the computer. 

Device removal is either global to all hardware profiles or specific to one hardware profile as specified by the <b>Scope</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553323">SP_REMOVEDEVICE_PARAMS</a> structure that supplies the class installation parameters for the DIF_REMOVE request. Configuration-specific removal is only appropriate for root-enumerated devices and should only be requested by system code. 

The caller of <b>SetupDiRemoveDevice</b> must be a member of the Administrators group.

<div class="alert"><b>Note</b>  Only a <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">class installer</a> should call <b>SetupDiRemoveDevice </b>and only in those situations where the class installer must perform device removal operations after <b>SetupDiRemoveDevice </b>completes the default device removal operation. In such situations, the class installer must directly call <b>SetupDiRemoveDevice</b> when the installer processes a DIF_REMOVE request. For more information about calling the default handler, see <a href="devinst.calling_the_default_dif_code_handlers">Calling Default DIF Code Handlers</a>. </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff553323">SP_REMOVEDEVICE_PARAMS</a>
 

 

