---
UID: NF:setupapi.SetupDiDeleteDeviceInterfaceData
title: SetupDiDeleteDeviceInterfaceData function
author: windows-sdk-content
description: The SetupDiDeleteDeviceInterfaceData function deletes a device interface from a device information set.
old-location: devinst\setupdideletedeviceinterfacedata.htm
old-project: devinst
ms.assetid: 20c9fe5b-ed88-4e2c-bca5-eba62f919fe6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetupDiDeleteDeviceInterfaceData, SetupDiDeleteDeviceInterfaceData function [Device and Driver Installation], devinst.setupdideletedeviceinterfacedata, di-rtns_6694af3a-5716-4ee6-b10e-2603dc341781.xml, setupapi/SetupDiDeleteDeviceInterfaceData
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
 - SetupDiDeleteDeviceInterfaceData
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiDeleteDeviceInterfaceData function


## -description


The <b>SetupDiDeleteDeviceInterfaceData</b> function deletes a device interface from a device information set.


## -parameters




### -param DeviceInfoSet [in]

A pointer to the <a href="devinst.device_information_sets">device information set</a> that contains the interface to delete. This handle is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>.


### -param DeviceInterfaceData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the interface in <i>DeviceInfoSet</i> to delete. This structure is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>.


## -returns



<b>SetupDiDeleteDeviceInterfaceData</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



<b>SetupDiDeleteDeviceInterfaceData</b> deletes a device interface element from a device information set. This function has no effect on the device interface or the underlying device.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552074">SetupDiOpenDeviceInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552102">SetupDiRemoveDeviceInterface</a>
 

 

