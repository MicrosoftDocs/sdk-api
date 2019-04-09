---
UID: NC:faxroute.PFAXROUTEENUMFILES
title: PFAXROUTEENUMFILES (faxroute.h)
author: windows-sdk-content
description: A fax routing method calls the FaxRouteEnumFiles callback function to enumerate the files in the fax file list associated with a received fax document.
old-location: fax\_mfax_faxrouteenumfiles.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_5f77.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FaxRouteEnumFiles, FaxRouteEnumFiles callback function [Fax Service], PFAXROUTEENUMFILES, PFAXROUTEENUMFILES callback, _mfax_faxrouteenumfiles, fax._mfax_faxrouteenumfiles, faxroute/FaxRouteEnumFiles
ms.topic: callback
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
 - FaxRouteEnumFiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFAXROUTEENUMFILES callback function


## -description


A fax routing method calls the <i>FaxRouteEnumFiles</i> callback function to enumerate the files in the fax file list associated with a received fax document.


<a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> passes a pointer to the <a href="https://msdn.microsoft.com/en-us/library/ms692860(v=VS.85).aspx">FaxRouteEnumFile</a> callback function if it calls <i>FaxRouteEnumFiles</i>.


## -parameters




### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.


### -param *Guid [in]

Type: <b>GUID*</b>

Pointer to a null-terminated Unicode character string that contains the GUID for the fax routing method.


### -param FileEnumerator [in]

Type: <b>PFAXROUTEENUMFILE</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms692860(v=VS.85).aspx">FaxRouteEnumFile</a> callback function defined by the fax routing extension. <i>FaxRouteEnumFile</i> receives the file names in the fax file list associated with the received fax document.


### -param Context [in, out]

Type: <b>PVOID</b>

Pointer to an extension-defined value that <i>FaxRouteEnumFiles</i> passes to the <a href="https://msdn.microsoft.com/en-us/library/ms692860(v=VS.85).aspx">FaxRouteEnumFile</a> function. The fax routing method can define this value.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax service passes a pointer to the <i>FaxRouteEnumFiles</i> callback function when the fax service calls the <a href="https://msdn.microsoft.com/en-us/library/ms692863(v=VS.85).aspx">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="https://msdn.microsoft.com/en-us/library/ms692881(v=VS.85).aspx">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEENUMFILES</b> data type defines a pointer to a <i>FaxRouteEnumFiles</i> function.

The fax routing extension DLL must supply the <a href="https://msdn.microsoft.com/en-us/library/ms692860(v=VS.85).aspx">FaxRouteEnumFile</a> function specified by the <i>FileEnumerator</i> parameter. The fax service calls <i>FaxRouteEnumFile</i> to enumerate the files in the fax file list for the fax routing method. The fax service calls <i>FaxRouteEnumFile</i> once for each file in the fax file list.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms684521(v=VS.85).aspx">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692881(v=VS.85).aspx">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692865(v=VS.85).aspx">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692860(v=VS.85).aspx">FaxRouteEnumFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692863(v=VS.85).aspx">FaxRouteInitialize</a>
 

 

