---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PFAXROUTEENUMFILE callback function


## -description


The <i>FaxRouteEnumFile</i> callback function receives the file names in the fax file list associated with a received fax document. This function receives a file name in the fax file list associated with a received fax document, and executes a procedure defined by the routing extension. It can return a nonzero value to proceed to the next file name in the fax file list, or zero to stop <a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a>.

<i>FaxRouteEnumFile</i> is a placeholder for a function name defined by the fax routing extension DLL. The <b>PFAXROUTEENUMFILE</b> data type is a pointer to a <i>FaxRouteEnumFile</i> function.


## -parameters




### -param JobId [in]

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.


### -param *GuidOwner [in]

Type: <b>GUID*</b>

Pointer to the GUID associated with the fax routing method that added the file to the fax file list. (This file is specified by the <i>FileName</i> parameter.) 


### -param *GuidCaller [in]

Type: <b>GUID*</b>

Pointer to the GUID associated with the fax routing method that called the <a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a> function. (<i>FaxRouteEnumFiles</i> passes a pointer to the <i>FaxRouteEnumFile</i> function.) Note that this parameter has the same value as the <i>Guid</i> parameter of <i>FaxRouteEnumFiles</i>. The <i>GuidCaller</i> parameter can be <b>NULL</b>.


### -param FileName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string. The fax service sets this variable to the fully qualified path and name of one file in the fax file list associated with the received fax document.


### -param Context [in, out]

Type: <b>PVOID</b>

Pointer to an extension-defined value supplied by the fax routing method identified by the <i>GuidCaller</i> parameter. This is an opaque value that the <a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a> function passes to <i>FaxRouteEnumFile</i>. 


## -returns



Type: <b>BOOL</b>

The function returns a nonzero value to continue enumeration, or zero to stop enumeration. 




## -remarks



The fax routing extension DLL must register the <i>FaxRouteEnumFile</i> callback function by passing its address to the <a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a> function.

For more information, see <a href="https://msdn.microsoft.com/6aa919ad-3c99-4e27-a462-5ad670cfb4e9">Fax File Lists</a>.




## -see-also




<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/779e7c8e-13b7-4495-b0b3-3b01594a88fb">FaxRouteEnumFiles</a>
 

 

