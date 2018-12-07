---
UID: NF:tapi3if.ITTAPI.RegisterRequestRecipient
title: ITTAPI::RegisterRequestRecipient
author: windows-sdk-content
description: The RegisterRequestRecipient method registers an application instance as being the proper one to handle assisted telephony requests.
old-location: tapi3\ittapi_registerrequestrecipient.htm
tech.root: tapi
ms.assetid: bee5348e-99f0-4168-9021-112fc16d8921
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITTAPI interface [TAPI 2.2],RegisterRequestRecipient method, ITTAPI.RegisterRequestRecipient, ITTAPI::RegisterRequestRecipient, RegisterRequestRecipient, RegisterRequestRecipient method [TAPI 2.2], RegisterRequestRecipient method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_registerrequestrecipient, tapi3.ittapi_registerrequestrecipient, tapi3if/ITTAPI::RegisterRequestRecipient
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI.RegisterRequestRecipient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI::RegisterRequestRecipient


## -description


The 
<b>RegisterRequestRecipient</b> method registers an application instance as being the proper one to handle assisted telephony requests.


## -parameters




### -param lRegistrationInstance [in]

Pointer to registration instance.


### -param lRequestMode [in]

Request mode.


### -param fEnable [in]

VARIANT_TRUE indicates that the caller wants to register as the handler; VARIANT_FALSE that it wants to unregister as the handler.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The TAPI object has not been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2b6d4f99-3ffe-44ce-9cb5-3fdd565085db">ITRequest</a>



<a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>



<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/6896a18a-75ff-4f43-81e2-7b828bb16ff6">MakeCall</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

