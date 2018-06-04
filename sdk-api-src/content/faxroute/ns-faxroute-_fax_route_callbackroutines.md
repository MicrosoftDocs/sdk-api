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
 

 

