---
UID: NN:tapi3if.IEnumCallingCard
title: IEnumCallingCard
author: windows-sdk-content
description: The IEnumCallingCard interface provides COM-standard enumeration methods for the ITCallingCard interface. The ITAddressTranslation::EnumerateCallingCards method returns a pointer to IEnumCallingCard.
old-location: tapi3\ienumcallingcard.htm
tech.root: tapi
ms.assetid: d2eed88b-9a01-4205-a35d-92a24e07a1e2
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IEnumCallingCard, IEnumCallingCard interface [TAPI 2.2], IEnumCallingCard interface [TAPI 2.2],described, _tapi3_ienumcallingcard, tapi3.ienumcallingcard, tapi3if/IEnumCallingCard
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
 - IEnumCallingCard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumCallingCard interface


## -description


The 
<b>IEnumCallingCard</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/09787cd2-56b5-4ed2-8783-f3c53ce2cc66">ITCallingCard</a> interface. The 
<a href="https://msdn.microsoft.com/93f3cea1-70da-41f0-a8d5-692468a21695">ITAddressTranslation::EnumerateCallingCards</a> method returns a pointer to 
<b>IEnumCallingCard</b>.

The 
<b>IEnumCallingCard</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumCallingCard</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumCallingCard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumCallingCard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb1a2ac3-12d1-42f0-9c73-c4d0d8a88700">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df0b4591-581b-4949-9212-ff4c92eec12c">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/406e4f37-86b6-46bf-97b9-e9944f56bc0d">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c24acc61-9e1a-42a5-bf0f-302f523b0978">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

