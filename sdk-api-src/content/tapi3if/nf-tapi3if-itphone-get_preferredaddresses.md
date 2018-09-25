---
UID: NF:tapi3if.ITPhone.get_PreferredAddresses
title: ITPhone::get_PreferredAddresses
author: windows-sdk-content
description: The get_PreferredAddresses method returns a collection of addresses that the phone is preferred for use on. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_get_preferredaddresses.htm
tech.root: tapi
ms.assetid: bda43c65-a1f9-4143-b808-2a4e61220b1b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_PreferredAddresses method, ITPhone.get_PreferredAddresses, ITPhone::get_PreferredAddresses, _tapi3_itphone_get_preferredaddresses, get_PreferredAddresses, get_PreferredAddresses method [TAPI 2.2], get_PreferredAddresses method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_preferredaddresses, tapi3if/ITPhone::get_PreferredAddresses
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
 - ITPhone.get_PreferredAddresses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPhone::get_PreferredAddresses


## -description


The 
<b>get_PreferredAddresses</b> method returns a collection of addresses that the phone is preferred for use on. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.

This method is intended for Visual Basic and scripting applications. C/C++ applications will find it more convenient to use the 
<a href="https://msdn.microsoft.com/d72f6877-eb89-400e-a1bc-393116a9666f">EnumerateAddresses</a> method.


## -parameters




### -param pAddresses [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface pointers.


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
The <i>pAddresses</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the collection object.

</td>
</tr>
</table>
 




## -remarks



If no usable addresses are present on the system, this method returns an empty collection.

A phone device declares itself as being preferred to an address or set of addresses by returning address/line IDs using the TAPI 2.x 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> function with device class tapi/line.

Although the 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method before calling 
<a href="https://msdn.microsoft.com/7bb15dc1-c1f0-4da5-8217-baedb45b70f7">EnumeratePreferredAddresses</a>. This is because the implementation of the phone object can open the phone and call 
<b>phoneGetID</b> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface returned by <b>ITPhone::get_PreferredAddresses</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/7bb15dc1-c1f0-4da5-8217-baedb45b70f7">EnumeratePreferredAddresses</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/823db8d1-e4e3-4cfb-a864-5ad57a44ebc6">get_Addresses</a>



<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a>
 

 

