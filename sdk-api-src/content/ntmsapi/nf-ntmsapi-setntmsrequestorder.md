---
UID: NF:ntmsapi.SetNtmsRequestOrder
title: SetNtmsRequestOrder function
author: windows-driver-content
description: The SetNtmsRequestOrder function sets the order that the specified request will be processed in the library queue.
old-location: fs\setntmsrequestorder.htm
old-project: Rsm
ms.assetid: d7171ce9-14d9-4fbc-b95f-19c502adedd0
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: SetNtmsRequestOrder, SetNtmsRequestOrder function [Files], _zaw_setntmsrequestorder, base.setntmsrequestorder, fs.setntmsrequestorder, ntmsapi/SetNtmsRequestOrder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntmsapi.dll
api_name:
-	SetNtmsRequestOrder
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetNtmsRequestOrder function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsRequestOrder</b> function sets the order that the specified request will be processed in the library queue.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpRequestId [in]

Unique identifier of a library request.


### -param dwOrderNumber [in]

Order that the request will be processed in the queue.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
 NTMS_CONTROL_ACCESS to the computer is denied. Other security errors are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The library request identifier is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A request object with the specified identifier cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



Currently NTMS_LM_MOUNT requests are sorted using the order number.

The order number set by the 
<b>SetNtmsRequestOrder</b> function is specific to the type of request because the types are processed in a predetermined order. For example, an NTMS_LM_DISMOUNT request is processed prior to an NTMS_LM_MOUNT request. Within a specific class of requests the queue can be ordered, however. The lower ordered requests are processed first; for example, 1 is the first request processed, 2 is the next request processed, and so forth.

To process a request immediately, an application can set the order number to 1. To defer processing, an application should set the order number to a very large number or 0xFFFFFFFF. The order number of a request, which currently has an order number of zero, cannot be changed.




## -see-also




<a href="https://msdn.microsoft.com/68617846-63c7-4a47-887a-ee49705753ce">GetNtmsRequestOrder</a>



<a href="removable_storage_manager_functions.htm">Library Control Functions</a>
 

 

