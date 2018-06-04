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

# SetupDiCreateDeviceInterfaceRegKeyW function


## -description


The <b>SetupDiCreateDeviceInterfaceRegKey</b> function creates a registry key for storing information about a device interface and returns a handle to the key.


## -parameters




### -param DeviceInfoSet [in]

A handle to a <a href="devinst.device_information_sets">device information set</a> that contains the interface for which to create a registry key. The device information set must not contain remote elements.


### -param DeviceInterfaceData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552342">SP_DEVICE_INTERFACE_DATA</a> structure that specifies the device interface in <i>DeviceInfoSet</i>. This pointer is possibly returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a>.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550965">SetupDiCreateDeviceInterface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550986">SetupDiDeleteDeviceInterfaceRegKey</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552075">SetupDiOpenDeviceInterfaceRegKey</a>
 

 

