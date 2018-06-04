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

# SetupDiEnumDeviceInterfaces function


## -description


The <b>SetupDiEnumDeviceInterfaces</b> function enumerates the device interfaces that are contained in a device information set. 


## -parameters




### -param DeviceInfoSet [in]

A pointer to a <a href="devinst.device_information_sets">device information set</a> that contains the device interfaces for which to return information. This handle is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552344">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiEnumDeviceInterfaces</b> constrains the enumeration to the interfaces that are supported by the specified device. If this parameter is <b>NULL</b>, repeated calls to <b>SetupDiEnumDeviceInterfaces</b> return information about the interfaces that are associated with all the device information elements in <i>DeviceInfoSet</i>. This pointer is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551010">SetupDiEnumDeviceInfo</a>.


### -param InterfaceClassGuid [in]

A pointer to a GUID that specifies the device interface class for the requested interface.


### -param MemberIndex [in]

A zero-based index into the list of interfaces in the device information set. The caller should call this function first with <i>MemberIndex</i> set to zero to obtain the first interface. Then, repeatedly increment <i>MemberIndex</i> and retrieve an interface until this function fails and <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_MORE_ITEMS.

If <i>DeviceInfoData</i> specifies a particular device, the <i>MemberIndex</i> is relative to only the interfaces exposed by that device.


### -param DeviceInterfaceData [out]

A pointer to a caller-allocated buffer that contains, on successful return, a completed <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that identifies an interface that meets the search parameters. The caller must set <i>DeviceInterfaceData</i>.<b>cbSize</b> to <b>sizeof</b>(SP_DEVICE_INTERFACE_DATA) before calling this function.


## -returns



<b>SetupDiEnumDeviceInterfaces</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, <b>FALSE</b> is returned and the error code for the failure can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Repeated calls to this function return an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure for a different device interface. This function can be called repeatedly to get information about interfaces in a device information set that are associated with a particular device information element or that are associated with all device information elements.

<i>DeviceInterfaceData</i> points to a structure that identifies a requested device interface. To get detailed information about an interface, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff551120">SetupDiGetDeviceInterfaceDetail</a>. The detailed information includes the name of the device interface that can be passed to a Win32 function such as <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> (described in Microsoft Windows SDK documentation) to get a handle to the interface.

See <a href="https://msdn.microsoft.com/9abc48f9-babf-407f-9046-c1e45cbbdc64">System Defined Device Interface Classes</a> for a list of available device interface classes.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551010">SetupDiEnumDeviceInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551120">SetupDiGetDeviceInterfaceDetail</a>
 

 

