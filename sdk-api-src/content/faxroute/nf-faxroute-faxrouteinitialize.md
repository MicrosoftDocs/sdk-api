---
UID: NF:faxroute.FaxRouteInitialize
title: FaxRouteInitialize function
author: windows-sdk-content
description: The fax service calls the FaxRouteInitialize function once, each time the service starts, to initialize the fax routing extension DLL. Each fax routing extension DLL must export the FaxRouteInitialize function.
old-location: fax\_mfax_faxrouteinitialize.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_54o5.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
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

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692881(v=VS.85).aspx">FAX_ROUTE_CALLBACKROUTINES</a> structure that contains pointers to the callback functions the fax service supplies. The structure contains pointers to the <a href="https://msdn.microsoft.com/en-us/library/ms692874(v=VS.85).aspx">FaxRouteAddFile</a>, <a href="https://msdn.microsoft.com/en-us/library/ms692858(v=VS.85).aspx">FaxRouteDeleteFile</a>, <a href="https://msdn.microsoft.com/en-us/library/ms692862(v=VS.85).aspx">FaxRouteGetFile</a>, <a href="https://msdn.microsoft.com/en-us/library/ms692864(v=VS.85).aspx">FaxRouteEnumFiles</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms692909(v=VS.85).aspx">FaxRouteModifyRoutingData</a> functions. 

                    

The fax routing extension DLL must store these pointers in a global variable for later use.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax routing extension DLL should not perform provider-specific initialization when the fax service calls the <a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function, described in MSDN. Instead, the extension should do this when the fax service calls the <b>FaxRouteInitialize</b> function.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms693451(v=VS.85).aspx">Fax Routing Extension Registration</a> and <a href="https://msdn.microsoft.com/en-us/library/ms684521(v=VS.85).aspx">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692881(v=VS.85).aspx">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692865(v=VS.85).aspx">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692874(v=VS.85).aspx">FaxRouteAddFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692858(v=VS.85).aspx">FaxRouteDeleteFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692864(v=VS.85).aspx">FaxRouteEnumFiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692862(v=VS.85).aspx">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692909(v=VS.85).aspx">FaxRouteModifyRoutingData</a>
 

 

