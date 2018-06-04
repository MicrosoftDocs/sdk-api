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

# SetupDiCreateDeviceInterfaceW function


## -description


The <b>SetupDiCreateDeviceInterface</b> function registers a device interface on a local system or a remote system. 


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a>. This set contains a device information element that represents the device for which to register an interface. This handle is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>. 


### -param DeviceInfoData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies the device information element in <i>DeviceInfoSet</i>.


### -param InterfaceClassGuid [in]

A pointer to a class GUID that specifies the interface class for the new interface.


### -param ReferenceString [in, optional]

A pointer to a NULL-terminated string that supplies a reference string. This pointer is optional and can be <b>NULL</b>. Reference strings are used only by a few bus drivers that use device interfaces as placeholders for software devices that are created on demand.


### -param CreationFlags [in]

Reserved. Must be zero.


### -param DeviceInterfaceData [out, optional]

A pointer to a caller-initialized <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure to receive information about the new device interface. This pointer is optional and can be <b>NULL</b>. If the structure is supplied, the caller must set the <b>cbSize</b> member of this structure to <b>sizeof(</b>SP_DEVICE_INTERFACE_DATA<b>)</b> before calling this function. For more information, see the following <b>Remarks</b> section.


## -returns



<b>SetupDiCreateDeviceInterface</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

<b>SetupDiCreateDeviceInterface</b> registers an interface for a device. If a device has more than one interface, call this function once for each interface being registered. 

If this function successfully registers an interface for the device that corresponds to the specified device information element, it also adds the interface to the interface list that is associated with the device information element in the specified device information set.

Before a registered interface can be used by applications and other system components the interface must be enabled by the driver for the device.

This function creates a registry key for the new device interface. Callers of this function can access nonvolatile storage under this key using <a href="https://msdn.microsoft.com/library/windows/hardware/ff552075">SetupDiOpenDeviceInterfaceRegKey</a>.

If <b>SetupDiCreateDeviceInterface</b> successfully creates a new device interface, but the caller-supplied buffer in the <i>DeviceInterfaceData</i> parameter is invalid, this function will return <b>FALSE</b> and a subsequent call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> will return ERROR_INVALID_USER_BUFFER. However, the function does create and register the new device interface. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552075">SetupDiOpenDeviceInterfaceRegKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552102">SetupDiRemoveDeviceInterface</a>
 

 

