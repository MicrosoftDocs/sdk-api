---
UID: NC:faxroute.PFAXROUTEMODIFYROUTINGDATA
title: PFAXROUTEMODIFYROUTINGDATA (faxroute.h)
description: A fax routing method calls the FaxRouteModifyRoutingData callback function to modify the routing data for a subsequent fax routing method.
helpviewer_keywords: ["FaxRouteModifyRoutingData","FaxRouteModifyRoutingData callback function [Fax Service]","PFAXROUTEMODIFYROUTINGDATA","PFAXROUTEMODIFYROUTINGDATA callback","_mfax_faxroutemodifyroutingdata","fax._mfax_faxroutemodifyroutingdata","faxroute/FaxRouteModifyRoutingData"]
old-location: fax\_mfax_faxroutemodifyroutingdata.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_7ae9.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteModifyRoutingData, FaxRouteModifyRoutingData callback function [Fax Service], PFAXROUTEMODIFYROUTINGDATA, PFAXROUTEMODIFYROUTINGDATA callback, _mfax_faxroutemodifyroutingdata, fax._mfax_faxroutemodifyroutingdata, faxroute/FaxRouteModifyRoutingData
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFAXROUTEMODIFYROUTINGDATA
 - faxroute/PFAXROUTEMODIFYROUTINGDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - FaxRoute.h
api_name:
 - FaxRouteModifyRoutingData
---

# PFAXROUTEMODIFYROUTINGDATA callback function


## -description

A fax routing method calls the <i>FaxRouteModifyRoutingData</i> callback function to modify the routing data for a subsequent fax routing method.

## -parameters

### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.

### -param RoutingGuid [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the GUID of the fax routing method to modify.

### -param RoutingData [in]

Type: <b>LPBYTE</b>

Pointer to a buffer that contains additional routing data defined by the routing extension. For more information, see the following Remarks section. 

                    

The fax routing method that calls the <i>FaxRouteModifyRoutingData</i> function and the routing method specified by the <i>RoutingGuid</i> parameter must interpret the data in the <i>RoutingData</i> parameter.

### -param RoutingDataSize [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is the size, in bytes, of the buffer pointed to by the <i>RoutingData</i> parameter.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The fax service passes a pointer to the <i>FaxRouteModifyRoutingData</i> function when the fax service calls <a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a>. The service passes the pointer in a <a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEMODIFYROUTINGDATA</b> data type defines a pointer to a <i>FaxRouteModifyRoutingData</i> function.

A fax routing method can call the <i>FaxRouteModifyRoutingData</i> callback function to change the routing information for a subsequent routing method. The function does this by modifying the <b>RoutingInfoData</b> member of the <a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route">FAX_ROUTE</a> structure that applies to the subsequent method. This allows a fax routing extension to retrieve user-defined routing data and to provide additional callback information to a different routing method. When the subsequent routing method executes, it processes the received fax transmission using the modified routing data.

The fax routing method specified by the <i>RoutingGuid</i> parameter must have a lower priority and must run after the calling routing method. The priority level determines the relative order in which the fax service calls the fax routing methods when the service receives a fax document.

## -see-also

<a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route">FAX_ROUTE</a>



<a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a>



<a href="/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemethod">FaxRouteMethod</a>