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

# RpcErrorSaveErrorInfo function


## -description


The 
<b>RpcErrorSaveErrorInfo</b> function returns all error information for an enumeration handle as a BLOB.


## -parameters




### -param EnumHandle [in]

Pointer to the enumeration handle.


### -param ErrorBlob [out]

Pointer to the BLOB containing the error information.


### -param BlobSize [out]

Size of <i>ErrorBlob</i>, in bytes.


## -returns



Successful completion returns RPC_S_OK. The 
<b>RpcErrorSaveErrorInfo</b> function call may fail if not enough memory is available.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The BLOB is allocated on the system heap, and the caller is the owner of the buffer. The block allocated on the system heap may be larger than <i>BlobSize</i>, but only <i>BlobSize</i> is used. The 
<b>RpcErrorSaveErrorInfo</b> function saves the entire chain of extended error information records associated with the enumeration handle, regardless of cursor position, and does not change the cursor position for the enumeration.

The BLOB may be saved and later retrieved using the 
<a href="https://msdn.microsoft.com/cbd171ee-cef3-4880-a26d-81267cb813e9">RpcErrorLoadErrorInfo</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://msdn.microsoft.com/cbd171ee-cef3-4880-a26d-81267cb813e9">RpcErrorLoadErrorInfo</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

