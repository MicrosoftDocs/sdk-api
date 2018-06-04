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

# SetupDiCreateDeviceInfoList function


## -description


The <b>SetupDiCreateDeviceInfoList</b> function creates an empty <a href="devinst.device_information_sets">device information set</a> and optionally associates the set with a <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> and a top-level window.


## -parameters




### -param ClassGuid [in, optional]

A pointer to the <b>GUID</b> of the device setup class to associate with the newly created device information set. If this parameter is specified, only devices of this class can be included in this device information set. If this parameter is set to <b>NULL</b>, the device information set is not associated with a specific device setup class.


### -param hwndParent [in, optional]

A handle to the top-level window to use for any user interface that is related to non-device-specific actions (such as a select-device dialog box that uses the global class driver list). This handle is optional and can be <b>NULL</b>. If a specific top-level window is not required, set <i>hwndParent</i> to <b>NULL</b>.


## -returns



The function returns a handle to an empty device information set if it is successful. Otherwise, it returns <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The caller of this function must delete the returned device information set when it is no longer needed by calling <b>SetupDiDestroyDeviceInfoList</b>. 

To create a device information list for a remote computer use <a href="https://msdn.microsoft.com/library/windows/hardware/ff550958">SetupDiCreateDeviceInfoListEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550958">SetupDiCreateDeviceInfoListEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550996">SetupDiDestroyDeviceInfoList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551101">SetupDiGetDeviceInfoListClass</a>
 

 

