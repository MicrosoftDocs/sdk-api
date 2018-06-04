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

# SetupDiAskForOEMDisk function


## -description


The <b>SetupDiAskForOEMDisk</b> function displays a dialog that asks the user for the path of an OEM installation disk.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> for the local computer. This set contains a device information element that represents the device that is being installed. 


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiAskForOEMDisk</b> associates the driver with the device that is being installed. If this parameter is <b>NULL</b>, <b>SetupDiAskForOEMDisk</b> associates the driver with the global class driver list for <i>DeviceInfoSet</i>.


## -returns



The function returns <b>TRUE</b> if it is successful and the <b>DriverPath</b> field of the SP_DEVINSTALLPARAMS structure is updated to reflect the new path. If the user cancels the dialog, the function returns <b>FALSE</b> and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_CANCELLED.




## -remarks



<b>SetupDiAskForOEMDisk</b> allows the user to browse local and network drives for OEM installation files. However, <b>SetupDiAskForOEMDisk</b> is primarily designed to obtain the path of an OEM driver on a local computer before selecting and installing the driver for a device on that computer.

Although this function will not fail if the device information set if for a remote computer, the result is of limited use because the device information set cannot subsequently be used with DIF_<i>Xxx</i> installation requests or <b>SetupDi</b><i>Xxx</i> functions that do not support operations on a remote computer.

In particular, the device information set cannot be used as input with a DIF_SELECTDEVICE installation request to select a driver for a device, followed by a DIF_INSTALLDEVICE installation request to install a device on a remote computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552121">SetupDiSelectOEMDrv</a>
 

 

