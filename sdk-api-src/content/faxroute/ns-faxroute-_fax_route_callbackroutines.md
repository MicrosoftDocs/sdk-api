---
UID: NS:faxroute._FAX_ROUTE_CALLBACKROUTINES
title: "_FAX_ROUTE_CALLBACKROUTINES"
author: windows-sdk-content
description: The FAX_ROUTE_CALLBACKROUTINES structure contains pointers to callback functions the fax service provides.
old-location: fax\_mfax_fax_route_callbackroutines_str.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_6ctu.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: "*PFAX_ROUTE_CALLBACKROUTINES, FAX_ROUTE_CALLBACKROUTINES, FAX_ROUTE_CALLBACKROUTINES structure [Fax Service], PFAX_ROUTE_CALLBACKROUTINES, PFAX_ROUTE_CALLBACKROUTINES structure pointer [Fax Service], _FAX_ROUTE_CALLBACKROUTINES, _mfax_fax_route_callbackroutines_str, fax._mfax_fax_route_callbackroutines_str, faxroute/FAX_ROUTE_CALLBACKROUTINES, faxroute/PFAX_ROUTE_CALLBACKROUTINES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: faxroute.h
req.include-header: 
req.redist: 
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
req.typenames: FAX_ROUTE_CALLBACKROUTINES, *PFAX_ROUTE_CALLBACKROUTINES
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
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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

Pointer to a <a href="https://msdn.microsoft.com/8c0e97ae-5d85-4271-a68a-7ad852b1615c">FaxRouteAddFile</a> callback function that a fax routing method uses to add a file to the fax file list associated with a received fax document.


### -field FaxRouteDeleteFile

Type: <b>PFAXROUTEDELETEFILE</b>

Pointer to a <a href="https://msdn.microsoft.com/44189520-42d9-4b1c-bb5a-f8da8bfc4c27">FaxRouteDeleteFile</a> callback function that a fax routing method uses to delete a file from the fax file list associated with a received fax document.


### -field FaxRouteGetFile

Type: <b>PFAXROUTEGETFILE</b>

Pointer to a <a href="https://msdn.microsoft.com/41acd3a8-269f-4c24-bb40-a8c5b24e1304">FaxRouteGetFile</a> callback function that a fax routing method uses to retrieve a specific file name from the fax file list associated with a received fax document.


### -field FaxRouteEnumFiles

Type: <b>PFAXROUTEENUMFILES</b>

Pointer to a <a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a> callback function that a fax routing method uses to enumerate the files in the fax file list associated with a received fax document.


### -field FaxRouteModifyRoutingData

Type: <b>PFAXROUTEMODIFYROUTINGDATA</b>

Pointer to a <a href="https://msdn.microsoft.com/eeb84e95-1a47-4768-9cb7-d6e7a2ee2048">FaxRouteModifyRoutingData</a> callback function that a fax routing method uses to modify the routing data associated with a subsequent fax routing method.


## -remarks



The fax routing extension DLL must store the pointers to these callback functions in a global variable for later use.

If the <b>SizeOfStruct</b> member is greater than sizeof(FAX_ROUTE_CALLBACKROUTINES), this indicates that the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure has been updated by Microsoft, and your application is using an earlier version. To maintain backward compatibility, changes will be appended to the original prototype of the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure. For example, new members for additional callback functions will be added sequentially after the <b>FaxRouteModifyRoutingData</b> member.

For more information, see <a href="https://msdn.microsoft.com/ed27d558-1c8f-496b-830f-a8c4675ff56f">Fax Routing Extension Registration</a> and <a href="https://msdn.microsoft.com/6aa919ad-3c99-4e27-a462-5ad670cfb4e9">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/0adb8e29-b0d5-4c2e-9c4c-713dd50ccf73">Fax Routing Extension Structures</a>



<a href="https://msdn.microsoft.com/8c0e97ae-5d85-4271-a68a-7ad852b1615c">FaxRouteAddFile</a>



<a href="https://msdn.microsoft.com/44189520-42d9-4b1c-bb5a-f8da8bfc4c27">FaxRouteDeleteFile</a>



<a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a>



<a href="https://msdn.microsoft.com/41acd3a8-269f-4c24-bb40-a8c5b24e1304">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/eeb84e95-1a47-4768-9cb7-d6e7a2ee2048">FaxRouteModifyRoutingData</a>
 

 

