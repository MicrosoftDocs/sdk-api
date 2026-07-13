---
UID: NC:faxroute.PFAXROUTEENUMFILES
title: PFAXROUTEENUMFILES (faxroute.h)
description: A fax routing method calls the FaxRouteEnumFiles callback function to enumerate the files in the fax file list associated with a received fax document.
helpviewer_keywords: ["FaxRouteEnumFiles","FaxRouteEnumFiles callback function [Fax Service]","PFAXROUTEENUMFILES","PFAXROUTEENUMFILES callback","_mfax_faxrouteenumfiles","fax._mfax_faxrouteenumfiles","faxroute/FaxRouteEnumFiles"]
old-location: fax\_mfax_faxrouteenumfiles.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_5f77.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteEnumFiles, FaxRouteEnumFiles callback function [Fax Service], PFAXROUTEENUMFILES, PFAXROUTEENUMFILES callback, _mfax_faxrouteenumfiles, fax._mfax_faxrouteenumfiles, faxroute/FaxRouteEnumFiles
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
 - PFAXROUTEENUMFILES
 - faxroute/PFAXROUTEENUMFILES
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
 - FaxRouteEnumFiles
---

# PFAXROUTEENUMFILES callback function


## -description

A fax routing method calls the <i>FaxRouteEnumFiles</i> callback function to enumerate the files in the fax file list associated with a received fax document.


<a href="/previous-versions/windows/desktop/fax/-mfax-faxroutingmethod">FaxRoutingMethod</a> passes a pointer to the <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfile">FaxRouteEnumFile</a> callback function if it calls <i>FaxRouteEnumFiles</i>.

## -parameters

### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.

### -param Guid [in]

Type: <b>GUID*</b>

Pointer to a null-terminated Unicode character string that contains the GUID for the fax routing method.

### -param FileEnumerator [in]

Type: <b>PFAXROUTEENUMFILE</b>

Pointer to a <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfile">FaxRouteEnumFile</a> callback function defined by the fax routing extension. <i>FaxRouteEnumFile</i> receives the file names in the fax file list associated with the received fax document.

### -param Context [in, out]

Type: <b>PVOID</b>

Pointer to an extension-defined value that <i>FaxRouteEnumFiles</i> passes to the <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfile">FaxRouteEnumFile</a> function. The fax routing method can define this value.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The fax service passes a pointer to the <i>FaxRouteEnumFiles</i> callback function when the fax service calls the <a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEENUMFILES</b> data type defines a pointer to a <i>FaxRouteEnumFiles</i> function.

The fax routing extension DLL must supply the <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfile">FaxRouteEnumFile</a> function specified by the <i>FileEnumerator</i> parameter. The fax service calls <i>FaxRouteEnumFile</i> to enumerate the files in the fax file list for the fax routing method. The fax service calls <i>FaxRouteEnumFile</i> once for each file in the fax file list.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-file-lists">Fax File Lists</a>.

## -see-also

<a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfile">FaxRouteEnumFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a>
