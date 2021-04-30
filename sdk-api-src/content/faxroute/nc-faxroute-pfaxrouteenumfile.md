---
UID: NC:faxroute.PFAXROUTEENUMFILE
title: PFAXROUTEENUMFILE (faxroute.h)
description: The FaxRouteEnumFile callback function receives the file names in the fax file list associated with a received fax document.
helpviewer_keywords: ["FaxRouteEnumFile","FaxRouteEnumFile callback function [Fax Service]","PFAXROUTEENUMFILE","PFAXROUTEENUMFILE callback","_mfax_faxrouteenumfile","fax._mfax_faxrouteenumfile","faxroute/FaxRouteEnumFile"]
old-location: fax\_mfax_faxrouteenumfile.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_3of9.htm
ms.date: 12/05/2018
ms.keywords: FaxRouteEnumFile, FaxRouteEnumFile callback function [Fax Service], PFAXROUTEENUMFILE, PFAXROUTEENUMFILE callback, _mfax_faxrouteenumfile, fax._mfax_faxrouteenumfile, faxroute/FaxRouteEnumFile
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
 - PFAXROUTEENUMFILE
 - faxroute/PFAXROUTEENUMFILE
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
 - FaxRouteEnumFile
---

# PFAXROUTEENUMFILE callback function


## -description

The <i>FaxRouteEnumFile</i> callback function receives the file names in the fax file list associated with a received fax document. This function receives a file name in the fax file list associated with a received fax document, and executes a procedure defined by the routing extension. It can return a nonzero value to proceed to the next file name in the fax file list, or zero to stop <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a>.

<i>FaxRouteEnumFile</i> is a placeholder for a function name defined by the fax routing extension DLL. The <b>PFAXROUTEENUMFILE</b> data type is a pointer to a <i>FaxRouteEnumFile</i> function.

## -parameters

### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.

### -param GuidOwner [in]

Type: <b>GUID*</b>

Pointer to the GUID associated with the fax routing method that added the file to the fax file list. (This file is specified by the <i>FileName</i> parameter.)

### -param GuidCaller [in]

Type: <b>GUID*</b>

Pointer to the GUID associated with the fax routing method that called the <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a> function. (<i>FaxRouteEnumFiles</i> passes a pointer to the <i>FaxRouteEnumFile</i> function.) Note that this parameter has the same value as the <i>Guid</i> parameter of <i>FaxRouteEnumFiles</i>. The <i>GuidCaller</i> parameter can be <b>NULL</b>.

### -param FileName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string. The fax service sets this variable to the fully qualified path and name of one file in the fax file list associated with the received fax document.

### -param Context [in, out]

Type: <b>PVOID</b>

Pointer to an extension-defined value supplied by the fax routing method identified by the <i>GuidCaller</i> parameter. This is an opaque value that the <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a> function passes to <i>FaxRouteEnumFile</i>.

## -returns

Type: <b>BOOL</b>

The function returns a nonzero value to continue enumeration, or zero to stop enumeration.

## -remarks

The fax routing extension DLL must register the <i>FaxRouteEnumFile</i> callback function by passing its address to the <a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a> function.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-file-lists">Fax File Lists</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">Fax Routing Extension Application Programming Interface Overview</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-extension-functions">Fax Routing Extension Functions</a>



<a href="/previous-versions/windows/desktop/api/faxroute/nc-faxroute-pfaxrouteenumfiles">FaxRouteEnumFiles</a>
