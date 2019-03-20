---
UID: NC:faxroute.PFAXROUTEADDFILE
title: PFAXROUTEADDFILE (faxroute.h)
author: windows-sdk-content
description: A fax routing method calls the FaxRouteAddFile callback function to add a file to the fax file list associated with a received fax document.
old-location: fax\_mfax_faxrouteaddfile.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_5k6d.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FaxRouteAddFile, FaxRouteAddFile callback function [Fax Service], PFAXROUTEADDFILE, PFAXROUTEADDFILE callback, _mfax_faxrouteaddfile, fax._mfax_faxrouteaddfile, faxroute/FaxRouteAddFile
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
 - FaxRouteAddFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


### -param *Guid [in]

Type: <b>GUID*</b>

Pointer to a null-terminated Unicode character string that contains the GUID for the fax routing method that is adding the file.


## -returns



Type: <b>LONG</b>

If the function succeeds, the return value is the file number of the file added to the fax file list associated with the received fax.

If the function fails, the return value is 1. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax service passes a pointer to the <i>FaxRouteAddFile</i> callback function when the fax service calls the <a href="https://msdn.microsoft.com/en-us/library/ms692863(v=VS.85).aspx">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="https://msdn.microsoft.com/en-us/library/ms692881(v=VS.85).aspx">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEADDFILE</b> data type defines a pointer to a <i>FaxRouteAddFile</i> function. 

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms684521(v=VS.85).aspx">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692881(v=VS.85).aspx">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692865(v=VS.85).aspx">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692858(v=VS.85).aspx">FaxRouteDeleteFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692862(v=VS.85).aspx">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692863(v=VS.85).aspx">FaxRouteInitialize</a>
 

 

