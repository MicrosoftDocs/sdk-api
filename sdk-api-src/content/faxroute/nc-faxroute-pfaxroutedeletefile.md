---
UID: NC:faxroute.PFAXROUTEDELETEFILE
title: PFAXROUTEDELETEFILE
author: windows-sdk-content
description: A fax routing method calls the FaxRouteDeleteFile callback function to delete a file from the fax file list associated with a received fax document.
old-location: fax\_mfax_faxroutedeletefile.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_3691.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: FaxRouteDeleteFile, FaxRouteDeleteFile callback function [Fax Service], PFAXROUTEDELETEFILE, PFAXROUTEDELETEFILE callback, _mfax_faxroutedeletefile, fax._mfax_faxroutedeletefile, faxroute/FaxRouteDeleteFile
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
 - FaxRouteDeleteFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the function fails, the return value is 1. To get extended error information, the fax service calls <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>, described in MSDN.




## -remarks



A fax routing method can use the <i>FaxRouteDeleteFile</i> function to remove a file that a different routing method added to the fax file list. For more information, see <a href="https://msdn.microsoft.com/6aa919ad-3c99-4e27-a462-5ad670cfb4e9">Fax File Lists</a>.

The fax service passes a pointer to the <i>FaxRouteDeleteFile</i> callback function when the fax service calls the <a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a> function. The service passes the pointer in a <a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a> structure.

The <b>PFAXROUTEDELETEFILE</b> data type defines a pointer to a <i>FaxRouteDeleteFile</i> function.

<div class="alert"><b>Note</b>  A fax routing method cannot remove the initial Tagged Image File Format Class F (TIFF Class F) file from the fax file list. For information about Tagged Image File Format (TIFF) files, see <a href="https://msdn.microsoft.com/d7840c10-6059-40ed-9040-50eefefc7349">Fax Image Format</a>. .</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/fb76a8d3-27e6-4bd7-87a9-2255653fa5e8">FAX_ROUTE_CALLBACKROUTINES</a>



<a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/339f7fb6-64eb-403e-91be-210501042a25">Fax Routing Extension Functions</a>



<a href="https://msdn.microsoft.com/8c0e97ae-5d85-4271-a68a-7ad852b1615c">FaxRouteAddFile</a>



<a href="https://msdn.microsoft.com/41acd3a8-269f-4c24-bb40-a8c5b24e1304">FaxRouteGetFile</a>



<a href="https://msdn.microsoft.com/6593762b-2a5a-4338-9958-efe0c7687729">FaxRouteInitialize</a>
 

 

