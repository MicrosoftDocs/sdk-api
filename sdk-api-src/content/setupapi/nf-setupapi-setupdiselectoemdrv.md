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

# SetupDiSelectOEMDrv function


## -description


The <b>SetupDiSelectOEMDrv</b> function selects a driver for a device information set or a particular device information element that uses an OEM path supplied by the user.


## -parameters




### -param hwndParent [in, optional]

A window handle that will be the parent of any dialogs created during the processing of this function. This parameter can be used to override the <b>hwndParent</b> field in the installation parameters block of the specified device information set or element. 


### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> for which to select a driver. 


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiSelectOEMDrv</b> associates the selected driver with the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSelectOEMDrv</b> associates the selected driver with the global class driver list for <i>DeviceInfoSet</i>.  


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiSelectOEMDrv </b>is primarily designed to select an OEM driver for a device on a local computer before installing the device on that computer. Although <b>SetupDiSelectOEMDrv</b> will not fail if the device information set is for a remote computer, the result is of limited use because the device information set cannot subsequently be used with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations on a remote computer. In particular, the device information set cannot be used as input with a DIF_INSTALLDEVICE installation request to install a device on a remote computer.

<b>SetupDiSelectOEMDrv</b> prompts the user for the OEM path and then calls the class installer to select a driver from the OEM path.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550905">SetupDiAskForOEMDisk</a>
 

 

