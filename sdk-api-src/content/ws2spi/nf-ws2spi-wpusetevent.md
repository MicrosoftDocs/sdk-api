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

# WPUSetEvent function


## -description



			The 
<b>WPUSetEvent</b> function sets the state of the specified event object to signaled. This call is safe for use within interrupt context.


## -parameters




### -param hEvent [in]

Handle that identifies an open event object.


### -param lpErrno [out]

Pointer to the error code.


## -returns




						If no error occurs, the 
<b>WPUSetEvent</b> function returns the value <b>TRUE</b>. Otherwise, <b>FALSE</b> is returned, and a specific error code is available in <i>lpErrno</i>.



<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEvent</i> parameter is not a valid event object handle.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/d8c6133b-e5a7-4936-a796-0930bb95fd0c">WPUCloseEvent</a>



<a href="https://msdn.microsoft.com/61e71e93-e35f-4122-bd4d-c103f652d2ca">WPUCreateEvent</a>



<a href="https://msdn.microsoft.com/a3385c77-899c-4772-88b9-fb3e0fab54e0">WPUResetEvent</a>
 

 

