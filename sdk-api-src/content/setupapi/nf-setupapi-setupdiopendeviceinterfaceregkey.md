---
UID: NF:setupapi.SetupDiOpenDeviceInterfaceRegKey
title: SetupDiOpenDeviceInterfaceRegKey function
author: windows-driver-content
description: The SetupDiOpenDeviceInterfaceRegKey function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.
old-location: devinst\setupdiopendeviceinterfaceregkey.htm
old-project: devinst
ms.assetid: 950dddcb-2a59-4c2d-826b-147e9acf401a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: SetupDiOpenDeviceInterfaceRegKey, SetupDiOpenDeviceInterfaceRegKey function [Device and Driver Installation], devinst.setupdiopendeviceinterfaceregkey, di-rtns_420dfbe9-7cb3-4ecb-9341-b40fbc76a50e.xml, setupapi/SetupDiOpenDeviceInterfaceRegKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: DesktopFor universal, call CM_Open_Device_Interface_Key
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
api_name:
-	SetupDiOpenDeviceInterfaceRegKey
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupDiOpenDeviceInterfaceRegKey function


## -description


The <b>SetupDiOpenDeviceInterfaceRegKey</b> function opens the registry subkey that is used by applications and drivers to store information that is specific to a device interface.


## -parameters




### -param DeviceInfoSet [in]

A pointer to a <a href="devinst.device_information_sets">device information set</a> that contains the device interface for which to open a registry subkey.


### -param DeviceInterfaceData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface. This pointer can be returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>.


### -param Reserved

Reserved. Must be zero.


### -param samDesired [in]

The requested registry security access to the registry subkey. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation. 


## -returns



<b>SetupDiOpenDeviceInterfaceRegKey</b> returns a handle to the opened registry key. If the function fails, it returns INVALID_HANDLE_VALUE. To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



Depending on the value that is passed in the <i>samDesired</i> parameter, it might be necessary for the caller of this function to be a member of the Administrators group.

Close the handle returned from by function by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=194543">RegCloseKey</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550967">SetupDiCreateDeviceInterfaceRegKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551015">SetupDiEnumDeviceInterfaces</a>
 

 

