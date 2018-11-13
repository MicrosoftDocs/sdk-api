---
UID: NS:faxroute._FAX_ROUTE_CALLBACKROUTINES
title: "_FAX_ROUTE_CALLBACKROUTINES"
author: windows-sdk-content
description: The FAX_ROUTE_CALLBACKROUTINES structure contains pointers to callback functions the fax service provides.
old-location: fax\_mfax_fax_route_callbackroutines_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_6ctu.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PFAX_ROUTE_CALLBACKROUTINES, FAX_ROUTE_CALLBACKROUTINES, FAX_ROUTE_CALLBACKROUTINES structure [Fax Service], PFAX_ROUTE_CALLBACKROUTINES, PFAX_ROUTE_CALLBACKROUTINES structure pointer [Fax Service], _FAX_ROUTE_CALLBACKROUTINES, _mfax_fax_route_callbackroutines_str, fax._mfax_fax_route_callbackroutines_str, faxroute/FAX_ROUTE_CALLBACKROUTINES, faxroute/PFAX_ROUTE_CALLBACKROUTINES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - FaxRoute.h
api_name:
 - FAX_ROUTE_CALLBACKROUTINES
product: Windows
targetos: Windows
req.typenames: FAX_ROUTE_CALLBACKROUTINES, *PFAX_ROUTE_CALLBACKROUTINES
req.redist: 
---

# _FAX_ROUTE_CALLBACKROUTINES structure


## -description


The <b>FAX_ROUTE_CALLBACKROUTINES</b> structure contains pointers to callback functions the fax service provides. A fax routing extension's routing methods can call these callback functions to manage the files in the fax file list associated with a received fax document.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure. The fax service sets this member to sizeof(FAX_ROUTE_CALLBACKROUTINES). For information about backward compatibility, see the following Remarks section.


### -field FaxRouteAddFile

Type: <b>PFAXROUTEADDFILE</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692874(v=VS.85).aspx">FaxRouteAddFile</a> callback function that a fax routing method uses to add a file to the fax file list associated with a received fax document.


### -field FaxRouteDeleteFile

Type: <b>PFAXROUTEDELETEFILE</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692858(v=VS.85).aspx">FaxRouteDeleteFile</a> callback function that a fax routing method uses to delete a file from the fax file list associated with a received fax document.


### -field FaxRouteGetFile

Type: <b>PFAXROUTEGETFILE</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692862(v=VS.85).aspx">FaxRouteGetFile</a> callback function that a fax routing method uses to retrieve a specific file name from the fax file list associated with a received fax document.


### -field FaxRouteEnumFiles

Type: <b>PFAXROUTEENUMFILES</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692864(v=VS.85).aspx">FaxRouteEnumFiles</a> callback function that a fax routing method uses to enumerate the files in the fax file list associated with a received fax document.


### -field FaxRouteModifyRoutingData

Type: <b>PFAXROUTEMODIFYROUTINGDATA</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692909(v=VS.85).aspx">FaxRouteModifyRoutingData</a> callback function that a fax routing method uses to modify the routing data associated with a subsequent fax routing method.


## -remarks



The fax routing extension DLL must store the pointers to these callback functions in a global variable for later use.

If the <b>SizeOfStruct</b> member is greater than sizeof(FAX_ROUTE_CALLBACKROUTINES), this indicates that the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure has been updated by Microsoft, and your application is using an earlier version. To maintain backward compatibility, changes will be appended to the original prototype of the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure. For example, new members for additional callback functions will be added sequentially after the <b>FaxRouteModifyRoutingData</b> member.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms693451(v=VS.85).aspx">Fax Routing Extension Registration</a> and <a href="https://msdn.microsoft.com/en-us/library/ms684521(v=VS.85).aspx">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692900(v=VS.85).aspx">Fax Routing Extension Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692874(v=VS.85).aspx">FaxRouteAddFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692858(v=VS.85).aspx">FaxRouteDeleteFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692864(v=VS.85).aspx">FaxRouteEnumFiles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692862(v=VS.85).aspx">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692909(v=VS.85).aspx">FaxRouteModifyRoutingData</a>
 

 

