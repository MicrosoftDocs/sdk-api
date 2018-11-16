---
UID: NF:tapi3if.ITAddress2.EnumeratePreferredPhones
title: ITAddress2::EnumeratePreferredPhones
author: windows-sdk-content
description: The EnumeratePreferredPhones method enumerates the preferred phone objects for this address.
old-location: tapi3\itaddress2_enumeratepreferredphones.htm
tech.root: Tapi
ms.assetid: a5a02f79-59b3-43f0-9b3b-fdd7839ba026
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumeratePreferredPhones, EnumeratePreferredPhones method [TAPI 2.2], EnumeratePreferredPhones method [TAPI 2.2],ITAddress2 interface, ITAddress2 interface [TAPI 2.2],EnumeratePreferredPhones method, ITAddress2.EnumeratePreferredPhones, ITAddress2::EnumeratePreferredPhones, _tapi3_itaddress2_enumeratepreferredphones, tapi3.itaddress2_enumeratepreferredphones, tapi3if/ITAddress2::EnumeratePreferredPhones
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
 - ITAddress2.EnumeratePreferredPhones
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
- ITAddress2.EnumeratePreferredPhones
: 
---

# ITAddress2::EnumeratePreferredPhones


## -description


The 
<b>EnumeratePreferredPhones</b> method enumerates the preferred phone objects for this address.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="https://msdn.microsoft.com/6cb17c83-86db-4d44-bbd3-80a0e52fec73">get_PreferredPhones</a> method.


## -parameters




### -param ppEnumPhone [out]

Pointer to the location where, on success, this method will place a pointer to an enumeration object that contains the returned list of phones.


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
There is not enough memory to allocate the enumeration object.

</td>
</tr>
</table>
 




## -remarks



A phone device declares itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> with device class tapi/line. If no phones are available for use with the address, this method produces an empty enumeration and returns S_OK.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a> interface returned by <b>ITAddress2::EnumeratePreferredPhones</b>. The application must call <b>Release</b> on the 
<b>IEnumPhone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/fa12508d-6224-4e11-a4a3-5ce5fff7b735">IEnumPhone</a>



<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>
 

 

