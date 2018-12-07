---
UID: NF:tapi3if.ITAddress2.get_PreferredPhones
title: ITAddress2::get_PreferredPhones
author: windows-sdk-content
description: The get_PreferredPhones method returns a collection of phone objects corresponding to the phone devices that are preferred for use with this address.
old-location: tapi3\itaddress2_get_preferredphones.htm
tech.root: tapi
ms.assetid: 6cb17c83-86db-4d44-bbd3-80a0e52fec73
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITAddress2 interface [TAPI 2.2],get_PreferredPhones method, ITAddress2.get_PreferredPhones, ITAddress2::get_PreferredPhones, _tapi3_itaddress2_get_preferredphones, get_PreferredPhones, get_PreferredPhones method [TAPI 2.2], get_PreferredPhones method [TAPI 2.2],ITAddress2 interface, tapi3.itaddress2_get_preferredphones, tapi3if/ITAddress2::get_PreferredPhones
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
 - ITAddress2.get_PreferredPhones
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress2::get_PreferredPhones


## -description


The 
<b>get_PreferredPhones</b> method returns a collection of phone objects corresponding to the phone devices that are preferred for use with this address.

This method is intended for Visual Basic and scripting applications. C/C++ applications should use the 
<a href="https://msdn.microsoft.com/a5a02f79-59b3-43f0-9b3b-fdd7839ba026">EnumeratePreferredPhones</a> method instead.


## -parameters




### -param pPhones [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface pointers.


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
The <i>pPhones</i> parameter is not a valid pointer.

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



A phone device declares itself as being preferred to an address or set of addresses by returning address/line IDs using 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> with device class tapi/line. If no phones are available for use with this address, the method produces an empty collection and returns S_OK.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface returned by <b>ITAddress2::get_PreferredPhones</b>. The application must call <b>Release</b> on the 
<b>ITPhone</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>
 

 

