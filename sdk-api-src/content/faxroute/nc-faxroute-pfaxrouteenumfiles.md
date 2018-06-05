---
UID: NC:faxroute.PFAXROUTEENUMFILES
title: PFAXROUTEENUMFILES
author: windows-sdk-content
description: A fax routing method calls the FaxRouteEnumFiles callback function to enumerate the files in the fax file list associated with a received fax document.
old-location: fax\_mfax_faxrouteenumfiles.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_5f77.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FaxRouteEnumFiles, FaxRouteEnumFiles callback function [Fax Service], PFAXROUTEENUMFILES, PFAXROUTEENUMFILES callback, _mfax_faxrouteenumfiles, fax._mfax_faxrouteenumfiles, faxroute/FaxRouteEnumFiles
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_SEND, *PFAX_SEND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	FaxRoute.h
api_name:
-	FaxRouteEnumFiles
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# PFAXROUTEENUMFILES callback function


## -description


A fax routing method calls the <i>FaxRouteEnumFiles</i> callback function to enumerate the files in the fax file list associated with a received fax document.


<a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> passes a pointer to the <a href="https://msdn.microsoft.com/f17881a4-ee16-47a1-897d-28c70871fa36">FaxRouteEnumFile</a> callback function if it calls <i>FaxRouteEnumFiles</i>.


## -parameters




### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.


### -param *Guid [in]

Type: <b>GUID*</b>

Pointer to a null-terminated Unicode character string that contains the GUID for the fax routing method.


### -param FileEnumerator [in]

Type: <b>PFAXROUTEENUMFILE</b>

Pointer to a <a href="https://msdn.microsoft.com/f17881a4-ee16-47a1-897d-28c70871fa36">FaxRouteEnumFile</a> callback function defined by the fax routing extension. <i>FaxRouteEnumFile</i> receives the file names in the fax file list associated with the received fax document.


### -param Context [in, out]

Type: <b>PVOID</b>

Pointer to an extension-defined value that <i>FaxRouteEnumFiles</i> passes to the <a href="https://msdn.microsoft.com/f17881a4-ee16-47a1-897d-28c70871fa36">FaxRouteEnumFile</a> function. The fax routing method can define this value.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



The fax service passes a pointer to the <i>FaxRouteEnumFiles</i> callback function when the fax service calls the <a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEENUMFILES</b> data type defines a pointer to a <i>FaxRouteEnumFiles</i> function.

The fax routing extension DLL must supply the <a href="https://msdn.microsoft.com/f17881a4-ee16-47a1-897d-28c70871fa36">FaxRouteEnumFile</a> function specified by the <i>FileEnumerator</i> parameter. The fax service calls <i>FaxRouteEnumFile</i> to enumerate the files in the fax file list for the fax routing method. The fax service calls <i>FaxRouteEnumFile</i> once for each file in the fax file list.

For more information, see <a href="https://msdn.microsoft.com/6aa919ad-3c99-4e27-a462-5ad670cfb4e9">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/f17881a4-ee16-47a1-897d-28c70871fa36">FaxRouteEnumFile</a>



<a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a>
 

 

