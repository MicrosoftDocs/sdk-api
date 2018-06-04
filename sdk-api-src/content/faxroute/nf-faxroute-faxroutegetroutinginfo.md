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

# FaxRouteGetRoutingInfo function


## -description


The <b>FaxRouteGetRoutingInfo</b> function queries the fax routing extension DLL to obtain routing configuration data for a specific fax device. Each fax routing extension DLL must export the <b>FaxRouteGetRoutingInfo</b> function.


## -parameters




### -param RoutingGuid [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that contains the GUID for the fax routing method.


### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies the identifier of the fax device to query.


### -param RoutingInfo [in]

Type: <b>LPBYTE</b>

Pointer to a buffer that receives the fax routing configuration data.


### -param RoutingInfoSize [out]

Type: <b>LPDWORD</b>

Pointer to an unsigned <b>DWORD</b> variable that specifies the size, in bytes, of the buffer pointed to by the <i>RoutingInfo</i> parameter. For more information, see the following Remarks section.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax service calls the <b>FaxRouteGetRoutingInfo</b> function twice. On the first call to the function the fax service passes a null pointer in the <i>RoutingInfo</i> parameter. The fax routing extension DLL must set the <i>RoutingInfoSize</i> parameter to the size required for the <i>RoutingInfo</i> buffer. The fax service calls <b>FaxRouteGetRoutingInfo</b> a second time with a valid pointer to the <i>RoutingInfo</i> buffer.




## -see-also




<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/7c18c63d-e30e-4308-9b3a-d1ec4546a0f3">FaxRouteSetRoutingInfo</a>
 

 

