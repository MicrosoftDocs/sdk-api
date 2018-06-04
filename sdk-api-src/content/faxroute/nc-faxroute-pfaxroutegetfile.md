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

# PFAXROUTEGETFILE callback function


## -description


A fax routing method calls the <b>FaxRouteGetFile</b> callback function to retrieve the name of a specific file from the fax file list associated with a received fax document.


## -parameters




### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.


### -param Index [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the requested file. 


### -param FileNameBuffer [out]

Type: <b>LPWSTR</b>

Pointer to a buffer that receives a null-terminated Unicode character string that contains the requested file name. For more information, see the following Remarks section. 


### -param RequiredSize [in, out]

Type: <b>LPDWORD</b>

Pointer to an unsigned <b>DWORD</b> variable. If the <i>FileNameBuffer</i> parameter is <b>NULL</b>, receives the required size, in bytes, of the buffer pointed to by the <i>FileNameBuffer</i> parameter. If <i>FileNameBuffer</i> parameter is not <b>NULL</b>, this variable indicates the output buffer size. For more information, see the following Remarks section.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax routing method must call the <i>FaxRouteGetFile</i> function twice. The first time the routing method calls <i>FaxRouteGetFile</i> it must pass a null pointer in the <i>FileNameBuffer</i> parameter. The fax service sets the <i>RequiredSize</i> parameter to the size required for the <i>FileNameBuffer</i> parameter. The fax routing method must allocate the memory required for the buffer from the heap specified by the <a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a> function, and call <i>FaxRouteGetFile</i> again. The second time the routing method calls <i>FaxRouteGetFile</i> it must pass a valid pointer in the <i>FileNameBuffer</i> parameter.

The fax service passes a pointer to the <i>FaxRouteGetFile</i> callback function when the fax service calls <a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a>. The service passes the pointer in a <a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEGETFILE</b> data type is a pointer to a <i>FaxRouteGetFile</i> function.

For more information, see <a href="https://msdn.microsoft.com/6aa919ad-3c99-4e27-a462-5ad670cfb4e9">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a>
 

 

