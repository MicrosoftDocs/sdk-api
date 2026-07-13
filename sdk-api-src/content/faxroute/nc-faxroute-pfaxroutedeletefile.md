---
UID: NC:faxroute.PFAXROUTEDELETEFILE
title: PFAXROUTEDELETEFILE (faxroute.h)
description: A fax routing method calls the FaxRouteDeleteFile callback function to delete a file from the fax file list associated with a received fax document.
helpviewer_keywords: ["FaxRouteDeleteFile","FaxRouteDeleteFile callback function [Fax Service]","PFAXROUTEDELETEFILE","PFAXROUTEDELETEFILE callback","_mfax_faxroutedeletefile","fax._mfax_faxroutedeletefile","faxroute/FaxRouteDeleteFile"]
old-location: fax\_mfax_faxroutedeletefile.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_3691.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteDeleteFile, FaxRouteDeleteFile callback function [Fax Service], PFAXROUTEDELETEFILE, PFAXROUTEDELETEFILE callback, _mfax_faxroutedeletefile, fax._mfax_faxroutedeletefile, faxroute/FaxRouteDeleteFile
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
 - PFAXROUTEDELETEFILE
 - faxroute/PFAXROUTEDELETEFILE
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
 - FaxRouteDeleteFile
---

# PFAXROUTEDELETEFILE callback function


## -description

A fax routing method calls the <i>FaxRouteDeleteFile</i> callback function to delete a file from the fax file list associated with a received fax document.

## -parameters

### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.

### -param FileName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string. The string contains the fully qualified path and name of the file to delete from the fax file list associated with the received fax document.

## -returns

Type: <b>LONG</b>

If the function succeeds, the return value is the file number of the file deleted from the fax file list associated with the received fax.

If the function fails, the return value is 1. To get extended error information, the fax service calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A fax routing method can use the <i>FaxRouteDeleteFile</i> function to remove a file that a different routing method added to the fax file list. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-file-lists">Fax File Lists</a>.

The fax service passes a pointer to the <i>FaxRouteDeleteFile</i> callback function when the fax service calls the <a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEDELETEFILE</b> data type defines a pointer to a <i>FaxRouteDeleteFile</i> function.

<div class="alert"><b>Note</b>  A fax routing method cannot remove the initial Tagged Image File Format Class F (TIFF Class F) file from the fax file list. For information about Tagged Image File Format (TIFF) files, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-image-format">Fax Image Format</a>. .</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/faxroute/ns-faxroute-fax_route_callbackroutines">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteaddfile">FaxRouteAddFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxroutegetfile">FaxRouteGetFile</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nf-faxroute-faxrouteinitialize">FaxRouteInitialize</a>