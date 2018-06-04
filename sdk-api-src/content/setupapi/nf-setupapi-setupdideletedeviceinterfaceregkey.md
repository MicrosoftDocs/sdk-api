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

# SetupDiDeleteDeviceInterfaceRegKey function


## -description


The <b>SetupDiDeleteDeviceInterfaceRegKey</b> function deletes the registry subkey that is used by applications and drivers to store interface-specific information. 


## -parameters




### -param DeviceInfoSet [in]

A pointer to a <a href="devinst.device_information_sets">device information set</a> that contains the interface for which to delete interface-specific information in the registry. The device information set must not contain remote elements.


### -param DeviceInterfaceData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i>. This pointer is possibly returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>.


### -param Reserved

Reserved. Must be zero.


## -returns



<b>SetupDiDeleteDeviceInterfaceRegKey</b> returns <b>TRUE</b> if it is successful; otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

<b>SetupDiDeleteDeviceInterfaceRegKey</b> deletes the subkey used by drivers and applications to store information about the device interface instance. This subkey was created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff550967">SetupDiCreateDeviceInterfaceRegKey</a> or by the driver's call to an associated <a href="https://msdn.microsoft.com/bdc977ec-825c-406b-871b-b28b0bdc135a">I/O manager routine</a>. <b>SetupDiDeleteDeviceInterfaceRegKey</b> does not affect the main registry key for the device interface instance nor any other subkeys that may have been created.

The <i>DeviceInfoSet</i> must only contain elements on the local computer.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550967">SetupDiCreateDeviceInterfaceRegKey</a>
 

 

