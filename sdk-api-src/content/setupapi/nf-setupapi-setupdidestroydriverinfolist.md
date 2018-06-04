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

# SetupDiDestroyDriverInfoList function


## -description


The <b>SetupDiDestroyDriverInfoList</b> function deletes a driver list.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains the driver list to delete.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be set to <b>NULL</b>. If this parameter is specified, <b>SetupDiDestroyDriverInfoList</b> deletes the driver list for the specified device. If this parameter is <b>NULL</b>, <b>SetupDiDestroyDriverInfoList</b> deletes the global class driver list that is associated with <i>DeviceInfoSet</i>.


### -param DriverType [in]

The type of driver list to delete, which must be one of the following values:





#### SPDIT_CLASSDRIVER

Delete a list of class drivers. If <i>DeviceInfoData</i> is <b>NULL</b>, this driver list type must be specified.



#### SPDIT_COMPATDRIVER

Delete a list of compatible drivers for the specified device. <i>DeviceInfoData</i> must be specified if this driver list type is specified.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the currently selected driver is a member of the list being deleted, the selection is reset.

If a class driver list is being deleted, the DI_FLAGSEX_DIDINFOLIST and DI_DIDCLASS flags are reset for the corresponding device information set or device information element. The DI_MULTMFGS flags is also reset.

If a compatible driver list is being destroyed, the DI_FLAGSEX_DIDCOMPATINFO and DI_DIDCOMPAT flags are reset for the corresponding device information element.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550917">SetupDiBuildDriverInfoList</a>
 

 

