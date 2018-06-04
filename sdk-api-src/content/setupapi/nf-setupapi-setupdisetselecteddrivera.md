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

# SetupDiSetSelectedDriverA function


## -description


The <b>SetupDiSetSelectedDriver</b> function sets, or resets, the selected driver for a device information element or the selected class driver for a device information set. 


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains the driver list from which to select a driver for a device information element or for the device information set.


### -param DeviceInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiSetSelectedDriver</b> sets, or resets, the selected driver for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiSetSelectedDriver</b> sets, or resets, the selected class driver for <i>DeviceInfoSet</i>.


### -param DriverInfoData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff553287">SP_DRVINFO_DATA</a> structure that specifies the driver to be selected. This parameter is optional and can be <b>NULL</b>. If this parameter and <i>DeviceInfoData</i> are supplied, the specified driver must be a member of a driver list that is associated with <i>DeviceInfoData</i>. If this parameter is specified and <i>DeviceInfoData</i> is <b>NULL</b>, the driver must be a member of the global class driver list for <i>DeviceInfoSet</i>. If this parameter is <b>NULL</b>, the selected driver is reset for the device information element, if <i>DeviceInfoData</i> is specified, or the device information set, if <i>DeviceInfoData</i> is <b>NULL</b>.

If the <i>DriverInfoData.</i><b>Reserved</b> is <b>NULL</b>, the caller is requesting a search for a driver node with the specified parameters (<b>DriverType</b>, <b>Description</b>, and <b>ProviderName</b>). If a match is found, that driver node is selected. The <b>Reserved</b> field is updated on output to reflect the actual driver node where the match was found. If a match is not found, the function fails and a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_INVALID_PARAMETER. 


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the caller of <b>SetupDiSetSelectedDriver</b> is a member of the Administrators group, the class of the device is set to the class of the selected driver, provided that the two classes are different.

If <i>DriverInfoData</i> is <b>NULL</b>, <b>SetupDiSetSelectedDriver</b> resets the selected driver. As a result, there is no selected driver. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552013">SetupDiGetSelectedDriver</a>
 

 

