---
UID: NC:faxroute.PFAXROUTEADDFILE
title: PFAXROUTEADDFILE
author: windows-driver-content
description: A fax routing method calls the FaxRouteAddFile callback function to add a file to the fax file list associated with a received fax document.
old-location: fax\_mfax_faxrouteaddfile.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_5k6d.htm
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: FaxRouteAddFile, FaxRouteAddFile callback function [Fax Service], PFAXROUTEADDFILE, PFAXROUTEADDFILE callback, _mfax_faxrouteaddfile, fax._mfax_faxrouteaddfile, faxroute/FaxRouteAddFile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FAX_SEND, *PFAX_SEND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	FaxRoute.h
api_name:
-	FaxRouteAddFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
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



The fax service passes a pointer to the <i>FaxRouteAddFile</i> callback function when the fax service calls the <a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEADDFILE</b> data type defines a pointer to a <i>FaxRouteAddFile</i> function. 

For more information, see <a href="https://msdn.microsoft.com/6aa919ad-3c99-4e27-a462-5ad670cfb4e9">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/44189520-42d9-4b1c-bb5a-f8da8bfc4c27">FaxRouteDeleteFile</a>



<a href="https://msdn.microsoft.com/41acd3a8-269f-4c24-bb40-a8c5b24e1304">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a>
 

 

