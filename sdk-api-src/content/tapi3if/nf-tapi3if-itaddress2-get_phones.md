---
UID: NF:tapi3if.ITAddress2.get_Phones
title: ITAddress2::get_Phones
author: windows-sdk-content
description: The get_Phones method returns a VARIANT pointer to an ITCollection of phone objects corresponding to the phone devices that can be used with this address.
old-location: tapi3\itaddress2_get_phones.htm
tech.root: Tapi
ms.assetid: 5cd82f34-1f3f-46a2-bad3-954dc5b93d87
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITAddress2 interface [TAPI 2.2],get_Phones method, ITAddress2.get_Phones, ITAddress2::get_Phones, _tapi3_itaddress2_get_phones, get_Phones, get_Phones method [TAPI 2.2], get_Phones method [TAPI 2.2],ITAddress2 interface, tapi3.itaddress2_get_phones, tapi3if/ITAddress2::get_Phones
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
 - ITAddress2.get_Phones
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITAddress2.get_Phones
: 
---

# ITAddress2::get_Phones


## -description


The 
<b>get_Phones</b> method returns a VARIANT pointer to an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of phone objects corresponding to the phone devices that can be used with this address.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="https://msdn.microsoft.com/674a9c35-8949-4935-9fa2-800fced6b57b">EnumeratePhones</a> method instead.


## -parameters




### -param pPhones [out]

Pointer to a VARIANT containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface pointers.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A phone device declares itself as being available on all addresses that support audio terminals by the TSP setting the PHONEFEATURE_GENERICPHONE bit in the <b>dwPhoneFeatures</b> member of the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure. A phone device can also declare itself as being preferred to an address or set of addresses by returning address/line IDs via 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> with device class tapi/line. If no phones are available for use with the address, this method produces an empty collection and returns S_OK.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface returned by <b>ITAddress2::get_Phones</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/674a9c35-8949-4935-9fa2-800fced6b57b">EnumeratePhones</a>



<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>
 

 

