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

# tapiRequestDrop function


## -description


Closes a call request made by a previous call to <a href="https://msdn.microsoft.com/51db5bf7-debc-4a76-ba55-283fb30ba3ae">tapiRequestMediaCall</a>.
<div class="alert"><b>Note</b>  The tapiRequestDrop function is nonfunctional and obsolete for all classes of Windows-based applications. It should not be used.</div><div> </div>

## -parameters




### -param hwnd

TBD


### -param wRequestID

Pointer to a 32-bit integer value that contains the ID of the call request.


#### - hWnd

Handle to the Windows process that issued this request.


## -returns



The function is obsolete and will always return an error code. 




## -see-also




<a href="https://msdn.microsoft.com/43ca86b0-0107-4937-b15a-47916e144527">Assisted Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

