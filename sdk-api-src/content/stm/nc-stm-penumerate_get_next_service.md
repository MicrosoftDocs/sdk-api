---
UID: NC:stm.PENUMERATE_GET_NEXT_SERVICE
title: PENUMERATE_GET_NEXT_SERVICE
author: windows-sdk-content
description: The EnumerateGetNextService function returns the next service entry in an enumeration started by CreateServiceEnumerationHandle.
old-location: rras\enumerategetnextservice.htm
old-project: rras
ms.assetid: 45d0ccaa-97d5-4a14-9983-dc0ca268ed4b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: EnumerateGetNextService, EnumerateGetNextService callback function [RAS], PENUMERATE_GET_NEXT_SERVICE, PENUMERATE_GET_NEXT_SERVICE callback, _mpr_enumerategetnextservice, rras.enumerategetnextservice, stm/EnumerateGetNextService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: stm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SEC_WINNT_CREDUI_CONTEXT_VECTOR, *PSEC_WINNT_CREDUI_CONTEXT_VECTOR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Stm.h
api_name:
 - EnumerateGetNextService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# PENUMERATE_GET_NEXT_SERVICE callback function


## -description


The 
<b>EnumerateGetNextService</b> function returns the next service entry in an enumeration started by 
<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a>.


## -parameters




### -param EnumerationHandle [in]

Handle that identifies the enumeration and specifies the subset of services on which the enumeration will operate. The handle is obtained from a call to 
<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a>.


### -param Service [out]

Pointer to an 
<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a> structure that contains the next service in the enumeration. The services are returned in no particular order, and each service in the subset is returned only once.


## -returns



If the function succeeds, the buffer pointed to by the <i>Service</i> parameter receives the next service in the enumeration. In this case the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more services exist with the specified criteria.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/68ed5662-ffa8-456b-b79c-a6fb27339262">CreateServiceEnumerationHandle</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

