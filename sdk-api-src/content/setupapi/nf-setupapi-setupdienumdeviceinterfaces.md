---
UID: NF:setupapi.SetupDiEnumDeviceInterfaces
title: SetupDiEnumDeviceInterfaces function
author: windows-sdk-content
description: The SetupDiEnumDeviceInterfaces function enumerates the device interfaces that are contained in a device information set.
old-location: devinst\setupdienumdeviceinterfaces.htm
tech.root: devinst
ms.assetid: 5095404d-2447-407e-99e2-dd3ef3c3b905
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: SetupDiEnumDeviceInterfaces, SetupDiEnumDeviceInterfaces function [Device and Driver Installation], devinst.setupdienumdeviceinterfaces, di-rtns_1fd59eb7-0934-4747-9a0e-81dac96c23ef.xml, setupapi/SetupDiEnumDeviceInterfaces
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupDiEnumDeviceInterfaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiEnumDeviceInterfaces function


## -description


The <b>SetupDiEnumDeviceInterfaces</b> function enumerates the device interfaces that are contained in a device information set. 


## -parameters




### -param DeviceInfoSet [in]

A pointer to a <a href="devinst.device_information_sets">device information set</a> that contains the device interfaces for which to return information. This handle is typically returned by <a href="https://msdn.microsoft.com/31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b">SetupDiGetClassDevs</a>.


### -param DeviceInfoData [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/9ad0ef4f-4a67-4f16-8bb1-2242dad0d041">SP_DEVINFO_DATA</a> structure that specifies a device information element in <i>DeviceInfoSet</i>. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <b>SetupDiEnumDeviceInterfaces</b> constrains the enumeration to the interfaces that are supported by the specified device. If this parameter is <b>NULL</b>, repeated calls to <b>SetupDiEnumDeviceInterfaces</b> return information about the interfaces that are associated with all the device information elements in <i>DeviceInfoSet</i>. This pointer is typically returned by <a href="https://msdn.microsoft.com/34df0557-eb86-4b00-bbd7-a4f0c1b82ff4">SetupDiEnumDeviceInfo</a>.


### -param InterfaceClassGuid [in]

A pointer to a GUID that specifies the device interface class for the requested interface.


### -param MemberIndex [in]

A zero-based index into the list of interfaces in the device information set. The caller should call this function first with <i>MemberIndex</i> set to zero to obtain the first interface. Then, repeatedly increment <i>MemberIndex</i> and retrieve an interface until this function fails and <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_MORE_ITEMS.

If <i>DeviceInfoData</i> specifies a particular device, the <i>MemberIndex</i> is relative to only the interfaces exposed by that device.


### -param DeviceInterfaceData [out]

A pointer to a caller-allocated buffer that contains, on successful return, a completed <a href="https://msdn.microsoft.com/df142e95-aa1c-4d3e-90c6-bac86effbd5d">SP_DEVICE_INTERFACE_DATA</a> structure that identifies an interface that meets the search parameters. The caller must set <i>DeviceInterfaceData</i>.<b>cbSize</b> to <b>sizeof</b>(SP_DEVICE_INTERFACE_DATA) before calling this function.


## -returns



<b>SetupDiEnumDeviceInterfaces</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, <b>FALSE</b> is returned and the error code for the failure can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Repeated calls to this function return an <a href="https://msdn.microsoft.com/df142e95-aa1c-4d3e-90c6-bac86effbd5d">SP_DEVICE_INTERFACE_DATA</a> structure for a different device interface. This function can be called repeatedly to get information about interfaces in a device information set that are associated with a particular device information element or that are associated with all device information elements.

<i>DeviceInterfaceData</i> points to a structure that identifies a requested device interface. To get detailed information about an interface, call <a href="https://msdn.microsoft.com/fb4963f1-0ed4-483d-9f39-dcbac493bf1d">SetupDiGetDeviceInterfaceDetail</a>. The detailed information includes the name of the device interface that can be passed to a Win32 function such as <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> (described in Microsoft Windows SDK documentation) to get a handle to the interface.

See <a href="https://msdn.microsoft.com/9abc48f9-babf-407f-9046-c1e45cbbdc64">System Defined Device Interface Classes</a> for a list of available device interface classes.




## -see-also




<a href="https://msdn.microsoft.com/34df0557-eb86-4b00-bbd7-a4f0c1b82ff4">SetupDiEnumDeviceInfo</a>



<a href="https://msdn.microsoft.com/31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/fb4963f1-0ed4-483d-9f39-dcbac493bf1d">SetupDiGetDeviceInterfaceDetail</a>
 

 

