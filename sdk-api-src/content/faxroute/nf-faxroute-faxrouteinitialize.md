---
UID: NF:faxroute.FaxRouteInitialize
title: FaxRouteInitialize function (faxroute.h)
author: windows-sdk-content
description: The fax service calls the FaxRouteInitialize function once, each time the service starts, to initialize the fax routing extension DLL. Each fax routing extension DLL must export the FaxRouteInitialize function.
old-location: fax\_mfax_faxrouteinitialize.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_54o5.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FaxRouteInitialize, FaxRouteInitialize function [Fax Service], _mfax_faxrouteinitialize, fax._mfax_faxrouteinitialize, faxroute/FaxRouteInitialize
ms.topic: function
f1_keywords: 
 - "faxroute/FaxRouteInitialize"
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FaxRouteInitialize function


## -description


The fax service calls the <b>FaxRouteInitialize</b> function once, each time the service starts, to initialize the fax routing extension DLL. Each fax routing extension DLL must export the <b>FaxRouteInitialize</b> function.


## -parameters




### -param HeapHandle [in]

Type: <b>HANDLE</b>

Handle to an initialized heap. The fax routing extension DLL must use the Win32 <a href="https://docs.microsoft.com/windows/desktop/Memory/heap-functions">heap functions</a>, described in MSDN, to allocate all memory from this heap.


### -param FaxRouteCallbackRoutines [in]

Type: <b>PFAX_ROUTE_CALLBACKROUTINES</b>

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/ns-faxroute-_fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a> structure that contains pointers to the callback functions the fax service supplies. The structure contains pointers to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteaddfile">FaxRouteAddFile</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutedeletefile">FaxRouteDeleteFile</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutegetfile">FaxRouteGetFile</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemodifyroutingdata">FaxRouteModifyRoutingData</a> functions. 

                    

The fax routing extension DLL must store these pointers in a global variable for later use.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, described in MSDN.




## -remarks



The fax routing extension DLL should not perform provider-specific initialization when the fax service calls the <a href="https://docs.microsoft.com/windows/desktop/Dlls/dllmain">DllMain</a> function, described in MSDN. Instead, the extension should do this when the fax service calls the <b>FaxRouteInitialize</b> function.

For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-registration">Fax Routing Extension Registration</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-file-lists">Fax File Lists</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/ns-faxroute-_fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteaddfile">FaxRouteAddFile</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutedeletefile">FaxRouteDeleteFile</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutegetfile">FaxRouteGetFile</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemodifyroutingdata">FaxRouteModifyRoutingData</a>
 

 

