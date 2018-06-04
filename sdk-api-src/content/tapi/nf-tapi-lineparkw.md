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

# lineParkW function


## -description


The 
<b>linePark</b> function parks the specified call according to the specified park mode.


## -parameters




### -param hCall

Handle to the call to be parked. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>connected</i>.


### -param dwParkMode

Park mode with which the call is to be parked. This parameter can have only a single flag set, and uses one of the 
<a href="https://msdn.microsoft.com/4b182c16-9d58-4244-bc5a-05c393800948">LINEPARKMODE_ Constants</a>.


### -param lpszDirAddress

Pointer to a <b>null</b>-terminated string that indicates the address where the call is to be parked when using directed park. The address is in dialable number format. This parameter is ignored for nondirected park.


### -param lpNonDirAddress

Pointer to a structure of type 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>. For nondirected park, the address where the call is parked is returned in this structure. This parameter is ignored for directed park. Within the 
<b>VARSTRING</b> structure, <b>dwStringFormat</b> must be set to STRINGFORMAT_ASCII (an ASCII string buffer containing a <b>null</b>-terminated string), and the terminating <b>NULL</b> must be accounted for in the <b>dwStringSize</b>. Prior to calling 
<b>linePark</b>, the application must set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALADDRESS, LINEERR_NOTOWNER, LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALPARKMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -remarks



With directed park, the application determines the address at which it wants to park the call. With nondirected park, the switch determines the address and provides this to the application. In either case, a parked call can be unparked by specifying this address.

The parked call typically enters the <i>idle</i> state after it has been successfully parked, and the application should then deallocate its handle to the call. If the application performs a 
<a href="https://msdn.microsoft.com/9262ab44-eac7-43e2-a0ec-dceea0838b09">lineUnpark</a> on the parked call, a new call handle is created for the unparked call even if the application has not deallocated its old call handle.

Some switches can remind the user after a call has been parked for some long amount of time. The application sees an <i>offering</i> call with a call reason set to <i>reminder</i>.

On a nondirected park, if the <b>dwTotalSize</b> member in the 
<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a> structure does not specify a sufficient amount of memory to receive the park address, the corresponding reply message returns a LINEERR_STRUCTURETOOSMALL error value. In such cases, there is no way to retrieve the complete park address. When a LINEERR_STRUCTURETOOSMALL error value is returned, the <b>dwNeededSize</b> member of the NonDirAddress structure does not contain a valid value. If a LINEERR_STRUCTURETOOSMALL error value is received from a nondirected 
<b>linePark</b>, then increase the size of the buffer and call 
<b>linePark</b> again until it returns either success or a different LINEERR_XXX result.




## -see-also




<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/6a82f03e-d8fd-4d0b-8f5d-f7934ba86759">Park Overview</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec73ed48-db5a-4478-8748-b8e58247c2f4">VARSTRING</a>



<a href="https://msdn.microsoft.com/9262ab44-eac7-43e2-a0ec-dceea0838b09">lineUnpark</a>
 

 

