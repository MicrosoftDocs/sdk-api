---
UID: NC:faxroute.PFAXROUTEADDFILE
title: PFAXROUTEADDFILE (faxroute.h)
description: A fax routing method calls the FaxRouteAddFile callback function to add a file to the fax file list associated with a received fax document.
helpviewer_keywords: ["FaxRouteAddFile","FaxRouteAddFile callback function [Fax Service]","PFAXROUTEADDFILE","PFAXROUTEADDFILE callback","_mfax_faxrouteaddfile","fax._mfax_faxrouteaddfile","faxroute/FaxRouteAddFile"]
old-location: fax\_mfax_faxrouteaddfile.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_5k6d.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteAddFile, FaxRouteAddFile callback function [Fax Service], PFAXROUTEADDFILE, PFAXROUTEADDFILE callback, _mfax_faxrouteaddfile, fax._mfax_faxrouteaddfile, faxroute/FaxRouteAddFile
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
 - PFAXROUTEADDFILE
 - faxroute/PFAXROUTEADDFILE
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
 - FaxRouteAddFile
---

# PFAXROUTEADDFILE callback function


## -description

A fax routing method calls the <i>FaxRouteAddFile</i> callback function to add a file to the fax file list associated with a received fax document.

## -parameters

### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.

### -param FileName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string. The string contains the fully qualified path and name of the file to add to the fax file list associated with the received fax document.

### -param Guid [in]

Type: <b>GUID*</b>

Pointer to a null-terminated Unicode character string that contains the GUID for the fax routing method that is adding the file.

## -returns

Type: <b>LONG</b>

If the function succeeds, the return value is the file number of the file added to the fax file list associated with the received fax.

If the function fails, the return value is 1. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The fax service passes a pointer to the <i>FaxRouteAddFile</i> callback function when the fax service calls the <a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEADDFILE</b> data type defines a pointer to a <i>FaxRouteAddFile</i> function. 

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-file-lists">Fax File Lists</a>.

## -see-also

<a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutedeletefile">FaxRouteDeleteFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutegetfile">FaxRouteGetFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a>
