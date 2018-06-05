---
UID: NF:tapi3if.ITPhone.get_Addresses
title: ITPhone::get_Addresses
author: windows-sdk-content
description: The get_Addresses method returns a collection of addresses that the phone can be used on. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_get_addresses.htm
old-project: Tapi
ms.assetid: 823db8d1-e4e3-4cfb-a864-5ad57a44ebc6
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITPhone interface [TAPI 2.2],get_Addresses method, ITPhone.get_Addresses, ITPhone::get_Addresses, _tapi3_itphone_get_addresses, get_Addresses, get_Addresses method [TAPI 2.2], get_Addresses method [TAPI 2.2],ITPhone interface, tapi3.itphone_get_addresses, tapi3if/ITPhone::get_Addresses
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPhone.get_Addresses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::get_Addresses


## -description


The 
<b>get_Addresses</b> method returns a collection of addresses that the phone can be used on. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="https://msdn.microsoft.com/d72f6877-eb89-400e-a1bc-393116a9666f">EnumerateAddresses</a> method instead.


## -parameters




### -param pAddresses [out]

Pointer to a VARIANT containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A phone device declares itself as being available on all addresses that support audio terminals by the TSP setting the PHONEFEATURE_GENERICPHONE bit in the <b>dwPhoneFeatures</b> member of the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure. A phone device can also declare itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> with device class tapi/line. The 
<b>get_Addresses</b> method returns addresses that have been identified both ways.

To get only addresses that the phone is preferred on, you can call the 
<a href="https://msdn.microsoft.com/bda43c65-a1f9-4143-b808-2a4e61220b1b">get_PreferredAddresses</a> method.

The application does not have to call the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method before calling 
<b>get_Addresses</b>. This is because the implementation of the phone object can open the phone and call 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface returned by <b>ITPhone::get_Addresses</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/bda43c65-a1f9-4143-b808-2a4e61220b1b">get_PreferredAddresses</a>
 

 

