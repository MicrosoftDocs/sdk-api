---
UID: NS:faxroute._FAX_ROUTE_CALLBACKROUTINES
title: FAX_ROUTE_CALLBACKROUTINES (faxroute.h)
description: The FAX_ROUTE_CALLBACKROUTINES structure contains pointers to callback functions the fax service provides.
helpviewer_keywords: ["*PFAX_ROUTE_CALLBACKROUTINES","FAX_ROUTE_CALLBACKROUTINES","FAX_ROUTE_CALLBACKROUTINES structure [Fax Service]","PFAX_ROUTE_CALLBACKROUTINES","PFAX_ROUTE_CALLBACKROUTINES structure pointer [Fax Service]","_mfax_fax_route_callbackroutines_str","fax._mfax_fax_route_callbackroutines_str","faxroute/FAX_ROUTE_CALLBACKROUTINES","faxroute/PFAX_ROUTE_CALLBACKROUTINES"]
old-location: fax\_mfax_fax_route_callbackroutines_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_6ctu.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_ROUTE_CALLBACKROUTINES, FAX_ROUTE_CALLBACKROUTINES, FAX_ROUTE_CALLBACKROUTINES structure [Fax Service], PFAX_ROUTE_CALLBACKROUTINES, PFAX_ROUTE_CALLBACKROUTINES structure pointer [Fax Service], _mfax_fax_route_callbackroutines_str, fax._mfax_fax_route_callbackroutines_str, faxroute/FAX_ROUTE_CALLBACKROUTINES, faxroute/PFAX_ROUTE_CALLBACKROUTINES'
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
targetos: Windows
req.typenames: FAX_ROUTE_CALLBACKROUTINES, *PFAX_ROUTE_CALLBACKROUTINES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_ROUTE_CALLBACKROUTINES
 - faxroute/_FAX_ROUTE_CALLBACKROUTINES
 - PFAX_ROUTE_CALLBACKROUTINES
 - faxroute/PFAX_ROUTE_CALLBACKROUTINES
 - FAX_ROUTE_CALLBACKROUTINES
 - faxroute/FAX_ROUTE_CALLBACKROUTINES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxRoute.h
api_name:
 - FAX_ROUTE_CALLBACKROUTINES
---

# FAX_ROUTE_CALLBACKROUTINES structure


## -description

The <b>FAX_ROUTE_CALLBACKROUTINES</b> structure contains pointers to callback functions the fax service provides. A fax routing extension's routing methods can call these callback functions to manage the files in the fax file list associated with a received fax document.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure. The fax service sets this member to sizeof(FAX_ROUTE_CALLBACKROUTINES). For information about backward compatibility, see the following Remarks section.

### -field FaxRouteAddFile

Type: <b>PFAXROUTEADDFILE</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteaddfile">FaxRouteAddFile</a> callback function that a fax routing method uses to add a file to the fax file list associated with a received fax document.

### -field FaxRouteDeleteFile

Type: <b>PFAXROUTEDELETEFILE</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutedeletefile">FaxRouteDeleteFile</a> callback function that a fax routing method uses to delete a file from the fax file list associated with a received fax document.

### -field FaxRouteGetFile

Type: <b>PFAXROUTEGETFILE</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutegetfile">FaxRouteGetFile</a> callback function that a fax routing method uses to retrieve a specific file name from the fax file list associated with a received fax document.

### -field FaxRouteEnumFiles

Type: <b>PFAXROUTEENUMFILES</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a> callback function that a fax routing method uses to enumerate the files in the fax file list associated with a received fax document.

### -field FaxRouteModifyRoutingData

Type: <b>PFAXROUTEMODIFYROUTINGDATA</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemodifyroutingdata">FaxRouteModifyRoutingData</a> callback function that a fax routing method uses to modify the routing data associated with a subsequent fax routing method.

## -remarks

The fax routing extension DLL must store the pointers to these callback functions in a global variable for later use.

If the <b>SizeOfStruct</b> member is greater than sizeof(FAX_ROUTE_CALLBACKROUTINES), this indicates that the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure has been updated by Microsoft, and your application is using an earlier version. To maintain backward compatibility, changes will be appended to the original prototype of the <b>FAX_ROUTE_CALLBACKROUTINES</b> structure. For example, new members for additional callback functions will be added sequentially after the <b>FaxRouteModifyRoutingData</b> member.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-registration">Fax Routing Extension Registration</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-fax-file-lists">Fax File Lists</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-structures">Fax Routing Extension Structures</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteaddfile">FaxRouteAddFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutedeletefile">FaxRouteDeleteFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutegetfile">FaxRouteGetFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemodifyroutingdata">FaxRouteModifyRoutingData</a>