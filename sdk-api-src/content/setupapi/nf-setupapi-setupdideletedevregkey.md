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

# SetupDiDeleteDevRegKey function


## -description


The <b>SetupDiDeleteDevRegKey</b> function deletes specified user-accessible registry keys that are associated with a device information element.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains a device information element that represents the device for which to delete registry keys. The device information set must not contain remote elements.


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param Scope [in]

The scope of the registry key to delete. The scope indicates where the information is located. The key can be global or hardware profile-specific. Can be one of the following values:





#### DICS_FLAG_GLOBAL

Delete the key that stores global configuration information. 



#### DICS_FLAG_CONFIGSPECIFIC

Delete the key that stores hardware profile-specific configuration information. 


### -param HwProfile [in]

If <i>Scope</i> is set to DICS_FLAG_CONFIGSPECIFIC, the <i>HwProfile</i> parameter specifies the hardware profile for which to delete the registry key. If <i>HwProfile</i> is 0, the key for the current hardware profile is deleted. If <i>HwProfile</i> is 0xFFFFFFFF, the registry key for all hardware profiles is deleted. 


### -param KeyType [in]

The type of registry storage key to delete. Can be one of the following values:





#### DIREG_DEV

Delete the device's <a href="https://msdn.microsoft.com/3be5c842-d1b6-4c34-8990-e23e2d08dd23">hardware key</a>.



#### DIREG_DRV

Delete the device's <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">software key</a>.



#### DIREG_BOTH

Delete both the hardware and software keys for the device.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550973">SetupDiCreateDevRegKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551997">SetupDiGetHwProfileList</a>
 

 

