---
UID: NF:setupapi.SetupDiRemoveDeviceInterface
title: SetupDiRemoveDeviceInterface function
author: windows-sdk-content
description: The SetupDiRemoveDeviceInterface function removes a registered device interface from the system.
old-location: devinst\setupdiremovedeviceinterface.htm
old-project: devinst
ms.assetid: 5eb92c58-150a-4e52-897f-e2a2da36743d
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: SetupDiRemoveDeviceInterface, SetupDiRemoveDeviceInterface function [Device and Driver Installation], devinst.setupdiremovedeviceinterface, di-rtns_8401d04f-f4a5-4214-88fe-2c1309978af9.xml, setupapi/SetupDiRemoveDeviceInterface
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
 - SetupDiRemoveDeviceInterface
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupDiRemoveDeviceInterface function


## -description


The <b>SetupDiRemoveDeviceInterface</b> function removes a registered device interface from the system.


## -parameters




### -param DeviceInfoSet [in]

A pointer to the <a href="devinst.device_information_sets">device information set</a> that contains the device interface to remove. This handle is typically returned by <b>SetupDiGetClassDevs</b>. 


### -param DeviceInterfaceData [in, out]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i> to remove. This pointer is typically returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>.

After the interface is removed, this function sets the SPINT_REMOVED flag in <i>DeviceInterfaceData</i><b>.Flags</b>. It also clears the SPINT_ACTIVE flag, but be aware that this flag should have already been cleared before this function was called.


## -returns



<b>SetupDiRemoveDeviceInterface</b> returns <b>TRUE</b> if the function completed without error. If the function completed with an error, it returns <b>FALSE</b> and the error code for the failure can be retrieved by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



The caller of this function must be a member of the Administrators group.

<b>SetupDiRemoveDeviceInterface</b> removes the specified device interface from the system. This includes deleting the associated registry key. 

Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550984">SetupDiDeleteDeviceInterfaceData</a> to delete the interface from a device information list.

A device interface must be disabled to be removed. If the interface is enabled, this function fails and <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_DEVICE_INTERFACE_ACTIVE. Disable an interface by using whatever interface-specific mechanism is provided (for example, an IOCTL). If the caller has no way to disable an interface and the interface must be removed, the caller must stop the underlying device by using <a href="https://msdn.microsoft.com/library/windows/hardware/ff550930">SetupDiChangeState</a>. Stopping the device disables all the interfaces exposed by the device. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550930">SetupDiChangeState</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550984">SetupDiDeleteDeviceInterfaceData</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551069">SetupDiGetClassDevs</a>
 

 

