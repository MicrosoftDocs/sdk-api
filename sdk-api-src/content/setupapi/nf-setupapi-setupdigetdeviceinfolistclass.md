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

# SetupDiGetDeviceInfoListClass function


## -description


The <b>SetupDiGetDeviceInfoListClass</b> function retrieves the GUID for the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> associated with a device information set if the set has an associated class.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> to query.


### -param ClassGuid [out]

A pointer to variable of type GUID that receives the GUID for the associated class.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified device information set does not have an associated class because a class GUID was not specified when the set was created with <a href="https://msdn.microsoft.com/library/windows/hardware/ff550956">SetupDiCreateDeviceInfoList</a>, the function fails. In this case, a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_ASSOCIATED_CLASS.

If a device information set is for a remote computer, use <a href="https://msdn.microsoft.com/library/windows/hardware/ff551103">SetupDiGetDeviceInfoListDetail</a> to get the associated remote computer handle and computer name.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550956">SetupDiCreateDeviceInfoList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551103">SetupDiGetDeviceInfoListDetail</a>
 

 

