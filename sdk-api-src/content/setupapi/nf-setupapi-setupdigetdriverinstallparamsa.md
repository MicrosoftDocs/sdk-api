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

# SetupDiGetDriverInstallParamsA function


## -description


The <b>SetupDiGetDriverInstallParams</b> function retrieves driver installation parameters for a device information set or a particular device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains a driver information element that represents the driver for which to retrieve installation parameters.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that contains a device information element that represents the device for which to retrieve installation parameters. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver that is a member of a driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiGetDriverInstallParams</b> retrieves information about a driver  that is a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff553287">SP_DRVINFO_DATA</a> structure that specifies the driver information element that represents the driver for which to retrieve installation parameters. If <i>DeviceInfoData</i> is supplied, the driver must be a member of the driver list for the device that is specified by <i>DeviceInfoData</i>. Otherwise, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>.


### -param DriverInstallParams [out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff553290">SP_DRVINSTALL_PARAMS</a> structure to receive the installation parameters for this driver. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552172">SetupDiSetDriverInstallParams</a>
 

 

