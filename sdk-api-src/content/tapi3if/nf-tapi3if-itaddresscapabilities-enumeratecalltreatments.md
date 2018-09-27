---
UID: NF:tapi3if.ITAddressCapabilities.EnumerateCallTreatments
title: ITAddressCapabilities::EnumerateCallTreatments
author: windows-sdk-content
description: The EnumerateCallTreatments method gets call treatments. This method is provided for applications written in C/C++ and Java.
old-location: tapi3\itaddresscapabilities_enumeratecalltreatments.htm
tech.root: tapi
ms.assetid: 34a967ba-7d1f-4841-95be-9e83f927379b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: EnumerateCallTreatments, EnumerateCallTreatments method [TAPI 2.2], EnumerateCallTreatments method [TAPI 2.2],ITAddressCapabilities interface, ITAddressCapabilities interface [TAPI 2.2],EnumerateCallTreatments method, ITAddressCapabilities.EnumerateCallTreatments, ITAddressCapabilities::EnumerateCallTreatments, _tapi3_itaddresscapabilities_enumeratecalltreatments, tapi3.itaddresscapabilities_enumeratecalltreatments, tapi3if/ITAddressCapabilities::EnumerateCallTreatments
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
 - ITAddressCapabilities.EnumerateCallTreatments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressCapabilities::EnumerateCallTreatments


## -description


The 
<b>EnumerateCallTreatments</b> method gets 
<a href="https://msdn.microsoft.com/c28c9200-dd51-48b2-905c-fbe37c83b00f">call treatments</a>. This method is provided for applications written in C/C++ and Java.


## -parameters




### -param ppEnumCallTreatment [out]

Pointer to call treatment enumeration.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

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



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/0e87ec06-7f3a-410c-9d54-7a67991e089c">IEnumBstr</a> interface returned by <b>ITAddressCapabilities::EnumerateCallTreatments</b>. The application must call <b>Release</b> on the 
<b>IEnumBstr</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/0e87ec06-7f3a-410c-9d54-7a67991e089c">IEnumBstr</a>



<a href="https://msdn.microsoft.com/36f452ce-9171-41da-b003-4c7df17790da">ITAddressCapabilities</a>
 

 

