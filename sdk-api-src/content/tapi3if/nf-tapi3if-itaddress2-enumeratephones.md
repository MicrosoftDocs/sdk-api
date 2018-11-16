---
UID: NF:tapi3if.ITAddress2.EnumeratePhones
title: ITAddress2::EnumeratePhones
author: windows-sdk-content
description: The EnumeratePhones method enumerates the phone objects corresponding to the phone devices that can be used with this address.
old-location: tapi3\itaddress2_enumeratephones.htm
tech.root: Tapi
ms.assetid: 674a9c35-8949-4935-9fa2-800fced6b57b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumeratePhones, EnumeratePhones method [TAPI 2.2], EnumeratePhones method [TAPI 2.2],ITAddress2 interface, ITAddress2 interface [TAPI 2.2],EnumeratePhones method, ITAddress2.EnumeratePhones, ITAddress2::EnumeratePhones, _tapi3_itaddress2_enumeratephones, tapi3.itaddress2_enumeratephones, tapi3if/ITAddress2::EnumeratePhones
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
 - ITAddress2.EnumeratePhones
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
- ITAddress2.EnumeratePhones
: 
---

# ITAddress2::EnumeratePhones


## -description


The 
<b>EnumeratePhones</b> method enumerates the phone objects corresponding to the phone devices that can be used with this address.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="https://msdn.microsoft.com/5cd82f34-1f3f-46a2-bad3-954dc5b93d87">get_Phones</a> method.


## -parameters




### -param ppEnumPhone [out]

Pointer to the new 
<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a> interface.


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
The <i>ppEnumPhone</i> parameter is not a valid pointer.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



A phone device declares itself as being available on all addresses that support audio terminals by the TSP setting the PHONEFEATURE_GENERICPHONE bit in the <b>dwPhoneFeatures</b> member of the 
<a href="https://msdn.microsoft.com/9549e30c-9425-4fb1-8ce5-f180a32f8e1f">PHONECAPS</a> structure. A phone device can also declare itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> with device class tapi/line. If no phones are available for use with the address, this method produces an empty enumeration and returns S_OK.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a> interface returned by <b>ITAddress2::EnumeratePhones</b>. The application must call <b>Release</b> on the 
<b>IEnumPhone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a>



<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>
 

 

