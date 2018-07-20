---
UID: NF:setupapi.SetupDiDeleteDeviceInterfaceRegKey
title: SetupDiDeleteDeviceInterfaceRegKey function
author: windows-sdk-content
description: The SetupDiDeleteDeviceInterfaceRegKey function deletes the registry subkey that is used by applications and drivers to store interface-specific information.
old-location: devinst\setupdideletedeviceinterfaceregkey.htm
old-project: devinst
ms.assetid: 470c96d4-b04f-4c9f-9ce3-9ba3d9ae49c1
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: SetupDiDeleteDeviceInterfaceRegKey, SetupDiDeleteDeviceInterfaceRegKey function [Device and Driver Installation], devinst.setupdideletedeviceinterfaceregkey, di-rtns_73c5871c-1386-4362-be95-e4e49a052cf5.xml, setupapi/SetupDiDeleteDeviceInterfaceRegKey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupDiDeleteDeviceInterfaceRegKey
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
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
 

 

