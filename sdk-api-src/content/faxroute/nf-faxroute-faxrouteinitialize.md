---
UID: NF:faxroute.FaxRouteInitialize
title: FaxRouteInitialize function
author: windows-sdk-content
description: The fax service calls the FaxRouteInitialize function once, each time the service starts, to initialize the fax routing extension DLL. Each fax routing extension DLL must export the FaxRouteInitialize function.
old-location: fax\_mfax_faxrouteinitialize.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_54o5.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxRouteInitialize, FaxRouteInitialize function [Fax Service], _mfax_faxrouteinitialize, fax._mfax_faxrouteinitialize, faxroute/FaxRouteInitialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: faxroute.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: FAX_SEND, *PFAX_SEND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxRoute.h
api_name:
 - FaxRouteInitialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FaxRouteInitialize function


## -description


The fax service calls the <b>FaxRouteInitialize</b> function once, each time the service starts, to initialize the fax routing extension DLL. Each fax routing extension DLL must export the <b>FaxRouteInitialize</b> function.


## -parameters




### -param HeapHandle [in]

Type: <b>HANDLE</b>

Handle to an initialized heap. The fax routing extension DLL must use the Win32 <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a>, described in MSDN, to allocate all memory from this heap.


### -param FaxRouteCallbackRoutines [in]

Type: <b>PFAX_ROUTE_CALLBACKROUTINES</b>

Pointer to a <a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a> structure that contains pointers to the callback functions the fax service supplies. The structure contains pointers to the <a href="https://msdn.microsoft.com/8c0e97ae-5d85-4271-a68a-7ad852b1615c">FaxRouteAddFile</a>, <a href="https://msdn.microsoft.com/44189520-42d9-4b1c-bb5a-f8da8bfc4c27">FaxRouteDeleteFile</a>, <a href="https://msdn.microsoft.com/41acd3a8-269f-4c24-bb40-a8c5b24e1304">FaxRouteGetFile</a>, <a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a>, and <a href="https://msdn.microsoft.com/eeb84e95-1a47-4768-9cb7-d6e7a2ee2048">FaxRouteModifyRoutingData</a> functions. 

                    

The fax routing extension DLL must store these pointers in a global variable for later use.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax routing extension DLL should not perform provider-specific initialization when the fax service calls the <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function, described in MSDN. Instead, the extension should do this when the fax service calls the <b>FaxRouteInitialize</b> function.

For more information, see <a href="https://msdn.microsoft.com/ed27d558-1c8f-496b-830f-a8c4675ff56f">Fax Routing Extension Registration</a> and <a href="https://msdn.microsoft.com/6aa919ad-3c99-4e27-a462-5ad670cfb4e9">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/8c0e97ae-5d85-4271-a68a-7ad852b1615c">FaxRouteAddFile</a>



<a href="https://msdn.microsoft.com/44189520-42d9-4b1c-bb5a-f8da8bfc4c27">FaxRouteDeleteFile</a>



<a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a>



<a href="https://msdn.microsoft.com/41acd3a8-269f-4c24-bb40-a8c5b24e1304">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/eeb84e95-1a47-4768-9cb7-d6e7a2ee2048">FaxRouteModifyRoutingData</a>
 

 

