---
UID: NF:tapi3if.ITPhone.EnumerateAddresses
title: ITPhone::EnumerateAddresses
author: windows-sdk-content
description: The EnumerateAddresses method enumerates the addresses that the phone can be used on. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_enumerateaddresses.htm
old-project: tapi
ms.assetid: d72f6877-eb89-400e-a1bc-393116a9666f
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: EnumerateAddresses, EnumerateAddresses method [TAPI 2.2], EnumerateAddresses method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],EnumerateAddresses method, ITPhone.EnumerateAddresses, ITPhone::EnumerateAddresses, _tapi3_itphone_enumerateaddresses, tapi3.itphone_enumerateaddresses, tapi3if/ITPhone::EnumerateAddresses
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
 - ITPhone.EnumerateAddresses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::EnumerateAddresses


## -description


The 
<b>EnumerateAddresses</b> method enumerates the addresses that the phone can be used on. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="https://msdn.microsoft.com/823db8d1-e4e3-4cfb-a864-5ad57a44ebc6">get_Addresses</a> method.


## -parameters




### -param ppEnumAddress [out]

Pointer to the 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If no phones are available for use with the address, this method produces an empty enumeration and returns S_OK.

A phone device declares itself as being available on all addresses that support audio terminals by the TSP setting the PHONEFEATURE_GENERICPHONE bit in the <b>dwPhoneFeatures</b> member of the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure. A phone device can also declare itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> with device class tapi/line. The 
<b>EnumerateAddresses</b> method returns addresses that have been identified both ways.

To get only addresses that the phone is preferred on, you can call the 
<a href="https://msdn.microsoft.com/7bb15dc1-c1f0-4da5-8217-baedb45b70f7">EnumeratePreferredAddresses</a> method.

A phone device declares itself as being specific to an address or set of addresses by returning address/line IDs using 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> with device class tapi/line. Although the 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method before calling 
<b>EnumerateAddresses</b>. This is because the implementation of the phone object can open the phone and call 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface returned by <b>ITPhone::EnumerateAddresses</b>. The application must call <b>Release</b> on the 
<b>IEnumAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/7bb15dc1-c1f0-4da5-8217-baedb45b70f7">EnumeratePreferredAddresses</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>
 

 

