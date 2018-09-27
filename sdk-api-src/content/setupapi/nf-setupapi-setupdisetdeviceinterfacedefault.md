---
UID: NF:setupapi.SetupDiSetDeviceInterfaceDefault
title: SetupDiSetDeviceInterfaceDefault function
author: windows-sdk-content
description: The SetupDiSetDeviceInterfaceDefault function sets a device interface as the default interface for a device interface class.
old-location: devinst\setupdisetdeviceinterfacedefault.htm
tech.root: devinst
ms.assetid: 1be4dd1e-6bef-4ef6-9db3-6725c27ec16d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SetupDiSetDeviceInterfaceDefault, SetupDiSetDeviceInterfaceDefault function [Device and Driver Installation], devinst.setupdisetdeviceinterfacedefault, di-rtns_3c21b60f-d837-4c08-8e1c-816bd88e9ba7.xml, setupapi/SetupDiSetDeviceInterfaceDefault
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows XP and later versions of Windows.
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
api_name:
 - SetupDiSetDeviceInterfaceDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiSetDeviceInterfaceDefault function


## -description


The <b>SetupDiSetDeviceInterfaceDefault</b> function sets a device interface as the default interface for a device interface class.


## -parameters




### -param DeviceInfoSet [in]

A handle to the <a href="devinst.device_information_sets">device information set</a> that contains the device interface to set as the default for a device interface class. 


### -param DeviceInterfaceData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/df142e95-aa1c-4d3e-90c6-bac86effbd5d">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i>. 


### -param Flags [in]

Not used, must be zero.


### -param Reserved

Reserved for future use, must be <b>NULL</b>.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



A caller must have Administrator privileges to set the default interface for a device interface class. However, if the requested default interface is the same as the currently set default interface, the function returns <b>TRUE</b> regardless of whether the caller has Administrator privileges. 

If the function successfully sets the specified device interface as the default for the device class, it updates the Flags member of the supplied SP_DEVICE_INTERFACE_DATA structure.

Call <a href="https://msdn.microsoft.com/31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b">SetupDiGetClassDevs</a> to obtain a <i>DevInfoSet</i> handle to a device information set that contains the device interface to set as the default for a device interface class. To obtain the <i>DeviceInterfaceData </i>pointer to the device interface element, call <a href="https://msdn.microsoft.com/5095404d-2447-407e-99e2-dd3ef3c3b905">SetupDiEnumDeviceInterfaces</a> to enumerate the interfaces in the device information set. To retrieve information about an enumerated interface, call <a href="https://msdn.microsoft.com/fb4963f1-0ed4-483d-9f39-dcbac493bf1d">SetupDiGetDeviceInterfaceDetail</a>.




## -see-also




<a href="https://msdn.microsoft.com/5095404d-2447-407e-99e2-dd3ef3c3b905">SetupDiEnumDeviceInterfaces</a>



<a href="https://msdn.microsoft.com/31bb0fc8-0fb8-4122-b9e8-5ff8fbbd903b">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/fb4963f1-0ed4-483d-9f39-dcbac493bf1d">SetupDiGetDeviceInterfaceDetail</a>
 

 

