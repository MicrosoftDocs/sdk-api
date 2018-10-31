---
UID: NF:setupapi.SetupDiCreateDeviceInterfaceRegKeyA
title: SetupDiCreateDeviceInterfaceRegKeyA function
author: windows-sdk-content
description: The SetupDiCreateDeviceInterfaceRegKey function creates a registry key for storing information about a device interface and returns a handle to the key.
old-location: devinst\setupdicreatedeviceinterfaceregkey.htm
tech.root: devinst
ms.assetid: 1be942a1-428d-4cc4-bc9f-9f21243c3d21
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetupDiCreateDeviceInterfaceRegKey, SetupDiCreateDeviceInterfaceRegKey function [Device and Driver Installation], SetupDiCreateDeviceInterfaceRegKeyA, SetupDiCreateDeviceInterfaceRegKeyW, devinst.setupdicreatedeviceinterfaceregkey, di-rtns_4b18b81a-e8ae-4d04-ae67-26cb21472e23.xml, setupapi/SetupDiCreateDeviceInterfaceRegKey
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiCreateDeviceInterfaceRegKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupDiCreateDeviceInterfaceRegKeyA function


## -description


The <b>SetupDiCreateDeviceInterfaceRegKey</b> function creates a registry key for storing information about a device interface and returns a handle to the key.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains the interface for which to create a registry key. The device information set must not contain remote elements.


### -param DeviceInterfaceData [in]

A pointer to an <a href="https://msdn.microsoft.com/df142e95-aa1c-4d3e-90c6-bac86effbd5d">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i>. This pointer is possibly returned by <a href="https://msdn.microsoft.com/e5f78c34-b61c-4fcb-b021-fb8d07c2d841">SetupDiCreateDeviceInterface</a>.


### -param Reserved

Reserved. Must be zero.


### -param samDesired [in]

The registry security access that the caller requests for the key that is being created. For information about registry security access values of type REGSAM, see the Microsoft Windows SDK documentation. 


### -param InfHandle [in, optional]

The handle to an open INF file that contains a <i>DDInstall</i> section to be executed for the newly-created key. This parameter is optional and can be <b>NULL</b>. If this parameter is not <b>NULL</b>, <i>InfSectionName</i> must be specified as well.


### -param InfSectionName [in, optional]

A pointer to the name of an INF <i>DDInstall</i> section in the INF file that is specified by <i>InfHandle</i>. This section is executed for the newly created key. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, <i>InfHandle</i> must be specified as well.


## -returns



If <b>SetupDiCreateDeviceInterfaceRegKey</b> succeeds, the function returns a handle to the requested registry key in which interface information can be stored and retrieved. If <b>SetupDiCreateDeviceInterfaceRegKey</b> fails, the function returns INVALID_HANDLE_VALUE. Call <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> to get extended error information.




## -remarks



The caller of this function must be a member of the Administrators group.

If the requested key for the device interface already exists, <b>SetupDiCreateDeviceInterfaceRegKey</b> returns a handle to that key; otherwise, <b>SetupDiCreateDeviceInterfaceRegKey</b> creates a new nonvolatile registry key for the specified device interface. Callers of this function can store private configuration data for the device interface in this key. The driver for the device can access this key using <b>Io</b><i>Xxx</i> routines.

Close the handle returned from this function by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=194543">RegCloseKey</a>.

For installations that use layout files (specified by the <b>LayoutFile</b> entry in an <a href="https://msdn.microsoft.com/53e30950-28a3-4ae3-a351-a917b02c84a5">INF Version section</a>), the layout file must be opened by a call to <b>SetupOpenAppendInfFile</b> (described in Windows SDK documentation) before <b>SetupDiCreateDeviceInterfaceRegKey</b> is called.

The device information set specified by <i>DeviceInfoSet</i> must only contain elements on the local computer.




## -see-also




<a href="https://msdn.microsoft.com/e5f78c34-b61c-4fcb-b021-fb8d07c2d841">SetupDiCreateDeviceInterface</a>



<a href="https://msdn.microsoft.com/470c96d4-b04f-4c9f-9ce3-9ba3d9ae49c1">SetupDiDeleteDeviceInterfaceRegKey</a>



<a href="https://msdn.microsoft.com/950dddcb-2a59-4c2d-826b-147e9acf401a">SetupDiOpenDeviceInterfaceRegKey</a>
 

 

