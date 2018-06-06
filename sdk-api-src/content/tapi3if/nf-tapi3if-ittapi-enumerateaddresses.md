---
UID: NF:tapi3if.ITTAPI.EnumerateAddresses
title: ITTAPI::EnumerateAddresses
author: windows-sdk-content
description: The EnumerateAddresses method enumerates the addresses that are currently available. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Addresses method.
old-location: tapi3\ittapi_enumerateaddresses.htm
old-project: Tapi
ms.assetid: b40a2071-24bf-470c-bfba-de23317e8652
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: EnumerateAddresses, EnumerateAddresses method [TAPI 2.2], EnumerateAddresses method [TAPI 2.2],ITTAPI interface, ITTAPI interface [TAPI 2.2],EnumerateAddresses method, ITTAPI.EnumerateAddresses, ITTAPI::EnumerateAddresses, _tapi3_ittapi_enumerateaddresses, tapi3.ittapi_enumerateaddresses, tapi3if/ITTAPI::EnumerateAddresses
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI.EnumerateAddresses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPI::EnumerateAddresses


## -description


The 
<b>EnumerateAddresses</b> method enumerates the addresses that are currently available. Provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/9e70ae94-20a2-4ba4-ab39-794f611011d8">get_Addresses</a> method.


## -parameters




### -param ppEnumAddress [out]

Pointer to the 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnumAddress</i> parameter is not a valid pointer.

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
 




## -remarks



An application typically uses this enumeration to check the capabilities of each address and determine which are useful for current purposes.

If an expected address is not found, this may indicate that the appropriate service provider has not been installed or is not working correctly.

TAPI calls the <b>Addref</b> method on the 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface returned by <b>ITTAPI::EnumerateAddresses</b>. The application must call the <b>Release</b> method on the 
<b>IEnumAddress</b> interface to free resources associated with it.

If an address is created or removed during a TAPI session, the application will be notified through the 
<a href="https://msdn.microsoft.com/06cfe56c-907f-49ed-8a7a-db31383a06f9">ITTAPIEventNotification</a> interface. If an address has been created, such as by installing a Plug and Play device, the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> returns the <b>TE_ADDRESSCREATE</b> member of the 
<a href="https://msdn.microsoft.com/606e9f99-d90c-4d4a-8dd5-2734c9bd2e7e">TAPIOBJECT_EVENT</a> enum. If an address is removed, <b>ITTAPIEventNotification::Event</b> returns <b>TE_ADDRESSREMOVE</b>. Calling 
<b>EnumerateAddresses</b> after these events will reflect the current addresses.




## -see-also




<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>



<a href="https://msdn.microsoft.com/9e70ae94-20a2-4ba4-ab39-794f611011d8">get_Addresses</a>
 

 

