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

# FaxRouteSetRoutingInfo function


## -description


The <b>FaxRouteSetRoutingInfo</b> function modifies routing configuration data for a specific fax device. Each fax routing extension DLL must export the <b>FaxRouteSetRoutingInfo</b> function.


## -parameters




### -param RoutingGuid [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that contains the GUID for the fax routing method.


### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies the device identifier of the fax device that will have its routing configuration data modified. 


### -param RoutingInfo [in]

Type: <b>const BYTE*</b>

Pointer to a buffer that provides the fax routing configuration data.


### -param RoutingInfoSize [in]

Type: <b>DWORD</b>

Specifies the size, in bytes, of the buffer pointed to by the <i>RoutingInfo</i> parameter.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax service calls the <b>FaxRouteSetRoutingInfo</b> function to modify routing configuration data for a specific fax device.




## -see-also




<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/e95ea880-7cc0-478a-a585-529347c8543d">FaxRouteGetRoutingInfo</a>
 

 

