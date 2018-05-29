---
UID: NF:tapi3if.ITPhone.EnumeratePreferredAddresses
title: ITPhone::EnumeratePreferredAddresses
author: windows-sdk-content
description: The EnumeratePreferredAddresses method enumerates the preferred addresses for the phone object. The application does not have to call ITPhone::Open before executing this method.
old-location: tapi3\itphone_enumeratepreferredaddresses.htm
old-project: Tapi
ms.assetid: 7bb15dc1-c1f0-4da5-8217-baedb45b70f7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: EnumeratePreferredAddresses, EnumeratePreferredAddresses method [TAPI 2.2], EnumeratePreferredAddresses method [TAPI 2.2],ITPhone interface, ITPhone interface [TAPI 2.2],EnumeratePreferredAddresses method, ITPhone.EnumeratePreferredAddresses, ITPhone::EnumeratePreferredAddresses, _tapi3_itphone_enumeratepreferredaddresses, tapi3.itphone_enumeratepreferredaddresses, tapi3if/ITPhone::EnumeratePreferredAddresses
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPhone.EnumeratePreferredAddresses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPhone::EnumeratePreferredAddresses


## -description


The 
<b>EnumeratePreferredAddresses</b> method enumerates the preferred addresses for the phone object. The application does not have to call 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> before executing this method.

This method is intended for C/C++ applications. Visual Basic and scripting applications must use the 
<a href="https://msdn.microsoft.com/823db8d1-e4e3-4cfb-a864-5ad57a44ebc6">get_Addresses</a> method.


## -parameters




### -param ppEnumAddress [out]

Pointer to a location where, on success, the method places a pointer to an enumeration object that contains the list of addresses. For more information, see the following Remarks section.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the enumeration object.

</td>
</tr>
</table>
 




## -remarks



If there are no usable addresses present on the system, this method produces an empty enumeration and returns S_OK.

A phone device declares itself as being preferred to an address or set of addresses by returning address/line IDs using the TAPI 2.x 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> function with device class tapi/line.

Although the 
<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a> function requires the handle to an open phone device, the application does not have to call the 
<a href="https://msdn.microsoft.com/d9efe2f7-3628-4e1f-b554-a6889d82a973">ITPhone::Open</a> method before calling 
<b>EnumeratePreferredAddresses</b>. This is because the implementation of the phone object can open the phone and call 
<b>phoneGetID</b> during TAPI initialization or when a new phone object appears.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a> interface returned by <b>ITPhone::EnumeratePreferredAddresses</b>. The application must call <b>Release</b> on the 
<b>IEnumAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/d72f6877-eb89-400e-a1bc-393116a9666f">EnumerateAddresses</a>



<a href="https://msdn.microsoft.com/bfe9f12e-ceb7-4120-8193-70feb2bc7c85">IEnumAddress</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/6a9c90ca-7a9e-43de-8075-240185658538">phoneGetID</a>
 

 

