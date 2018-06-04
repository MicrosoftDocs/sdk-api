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

# EnumDeviceDrivers function


## -description


Retrieves the load address for each device driver in the system.


## -parameters




### -param lpImageBase [out]

An array that receives the list of load addresses for the device drivers.


### -param cb [in]

The size of the <i>lpImageBase</i> array, in bytes. If the array is not large enough to store the load addresses, the <i>lpcbNeeded</i> parameter receives the required size of the array.


### -param lpcbNeeded [out]

The number of bytes returned in the <i>lpImageBase</i> array.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To determine how many device drivers were enumerated by the call to 
<b>EnumDeviceDrivers</b>, divide the resulting value in the <i>lpcbNeeded</i> parameter by <code>sizeof(LPVOID)</code>.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and the library that a program must load. 

If PSAPI_VERSION is 2 or greater, this function is defined as <b>K32EnumDeviceDrivers</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If PSAPI_VERSION is 1, this function is defined as <b>EnumDeviceDrivers</b> in Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls <b>K32EnumDeviceDrivers</b>. 

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions should always call this function as <b>EnumDeviceDrivers</b>. To ensure correct resolution of symbols, add Psapi.lib to the TARGETLIBS macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load Psapi.dll.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/047d8541-e17e-4738-8453-674db69365df">Enumerating all Device Drivers in the System</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4f4ec15b-5592-4fe3-b754-fda25ab24159">Device Driver Information</a>



<a href="https://msdn.microsoft.com/a19a927d-4669-4d4c-951e-43f294a8fb40">GetDeviceDriverBaseName</a>



<a href="https://msdn.microsoft.com/6ddbcf7e-e41c-4ea7-b60a-01ed5c98c530">GetDeviceDriverFileName</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>
 

 

