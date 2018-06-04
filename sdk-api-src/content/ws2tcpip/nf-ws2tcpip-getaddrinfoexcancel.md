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

# GetAddrInfoExCancel function


## -description


The 
<b>GetAddrInfoExCancel</b> function cancels an asynchronous operation by the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function.


## -parameters




### -param lpHandle [in]

The handle of the asynchronous operation to cancel. This is the handle returned in the <i>lpNameHandle</i> parameter by the <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> function. 


## -returns




						On success,  <b>GetAddrInfoExCancel</b> returns <b>NO_ERROR</b> (0). Failure returns a nonzero Windows Sockets error code, as found in the 
<a href="https://msdn.microsoft.com/50b924f3-2c88-443b-8a90-4293fe5c3048">Windows Sockets Error Codes</a>.




## -remarks



The <b>GetAddrInfoExCancel</b> function cancels an asynchronous <a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a> operation. The result is that the user's completion
    mechanism, either a callback or an event, is immediately invoked. No results are returned,
    and the error code returned for the <b>GetAddrInfoEx</b> asynchronous operation is set to <b>WSA_E_CANCELLED</b>. If the <b>GetAddrInfoEx</b> request has already completed or timed out,
    or the handle is invalid, and <b>WSA_INVALID_HANDLE</b> will be returned by <b>GetAddrInfoExCancel</b> function.


Since many of the underlying operations (legacy name service providers, for example) are synchronous, these operations
    will not actually be cancelled. These operations will continue running and consuming resources. Once the
    last outstanding name service provider request has completed, the resources will be released. 

<b>Windows 8.1</b> and <b>Windows Server 2012 R2</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and later.




## -see-also




<a href="https://msdn.microsoft.com/cc4ccb2d-ea5a-48bd-a3ae-f70432ab2c39">GetAddrInfoEx</a>
 

 

