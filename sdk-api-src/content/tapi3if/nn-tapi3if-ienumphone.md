---
UID: NN:tapi3if.IEnumPhone
title: IEnumPhone
author: windows-sdk-content
description: The IEnumPhone interface provides COM-standard enumeration methods for the ITPhone interface. The ITAddress2::EnumeratePhones and ITTAPI2::EnumeratePhones methods return a pointer to IEnumPhone.
old-location: tapi3\ienumphone.htm
tech.root: tapi
ms.assetid: fa12508d-6224-4e11-a4a3-5ce5fff7b735
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IEnumPhone, IEnumPhone interface [TAPI 2.2], IEnumPhone interface [TAPI 2.2],described, _tapi3_ienumphone, tapi3.ienumphone, tapi3if/IEnumPhone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IEnumPhone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumPhone interface


## -description


The 
<b>IEnumPhone</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a> interface. The 
<a href="https://msdn.microsoft.com/674a9c35-8949-4935-9fa2-800fced6b57b">ITAddress2::EnumeratePhones</a> and 
<a href="https://msdn.microsoft.com/6b6aba8d-fbf7-459f-9bc8-79647194b989">ITTAPI2::EnumeratePhones</a> methods return a pointer to 
<b>IEnumPhone</b>.

The 
<b>IEnumPhone</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumPhone</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumPhone</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumPhone</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b55bb1f5-ecde-4565-97b6-29e79823b9cb">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ea1e851-00df-4b32-ba37-c562da983102">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/394e1d55-56f2-4233-93ce-a109906414f4">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe137da2-2c12-4732-9ab8-adf07381c692">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/674a9c35-8949-4935-9fa2-800fced6b57b">ITAddress2::EnumeratePhones</a>



<a href="https://msdn.microsoft.com/94dff33c-67a1-4df8-9ef5-2b6524438f6f">ITPhone</a>



<a href="https://msdn.microsoft.com/6b6aba8d-fbf7-459f-9bc8-79647194b989">ITTAPI2::EnumeratePhones</a>
 

 

