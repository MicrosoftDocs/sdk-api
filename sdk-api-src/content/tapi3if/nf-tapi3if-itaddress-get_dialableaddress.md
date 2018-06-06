---
UID: NF:tapi3if.ITAddress.get_DialableAddress
title: ITAddress::get_DialableAddress
author: windows-sdk-content
description: The get_DialableAddress method gets the BSTR which can be used to connect to this address. The BSTR corresponds to the destination address string that another application would use to connect to this address, such as a phone number or an e-mail name.
old-location: tapi3\itaddress_get_dialableaddress.htm
old-project: Tapi
ms.assetid: 8d6dcbbe-3372-4346-8f5e-fb34b7aca88d
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_DialableAddress method, ITAddress.get_DialableAddress, ITAddress::get_DialableAddress, _tapi3_itaddress_get_dialableaddress, get_DialableAddress, get_DialableAddress method [TAPI 2.2], get_DialableAddress method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_dialableaddress, tapi3if/ITAddress::get_DialableAddress
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
 - ITAddress.get_DialableAddress
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddress::get_DialableAddress


## -description


The 
<b>get_DialableAddress</b> method gets the <b>BSTR</b> which can be used to connect to this address. The <b>BSTR</b> corresponds to the destination address string that another application would use to connect to this address, such as a phone number or an e-mail name.


## -parameters




### -param pDialableAddress [out]

Pointer to <b>BSTR</b> containing the dialable address string. This will match the <i>pDestAddress</i> argument of 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDialableAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>pDialableAddress</i> parameter.
			

The availability of this value depends on the service provider. For example, on an address exposed by the Unimodem service provider, this method will return an empty string instead of a phone number.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="address_ovr.htm">Dialable Addresses</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>
 

 

