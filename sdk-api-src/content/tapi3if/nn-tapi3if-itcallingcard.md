---
UID: NN:tapi3if.ITCallingCard
title: ITCallingCard
author: windows-sdk-content
description: The ITCallingCard interface provides methods to retrieve information concerning telephony calling cards.
old-location: tapi3\itcallingcard.htm
tech.root: Tapi
ms.assetid: 09787cd2-56b5-4ed2-8783-f3c53ce2cc66
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITCallingCard, ITCallingCard interface [TAPI 2.2], ITCallingCard interface [TAPI 2.2],described, _tapi3_itcallingcard, tapi3.itcallingcard, tapi3if/ITCallingCard
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITCallingCard
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallingCard interface


## -description


The 
<b>ITCallingCard</b> interface provides methods to retrieve information concerning telephony calling cards.

An 
<b>ITCallingCard</b> interface pointer can be obtained using 
<a href="https://msdn.microsoft.com/3033c584-1a7b-4bba-a8a2-2a2d59247689">ITAddressTranslation::get_CallingCards</a> or 
<a href="https://msdn.microsoft.com/93f3cea1-70da-41f0-a8d5-692468a21695">ITAddressTranslation::EnumerateCallingCards</a>.

<b>TAPI 2.1 Cross-Reference: </b>The information obtainable using this interface parallels that contained in the 
<a href="https://msdn.microsoft.com/8b2a4eaf-6c59-4d3b-839f-52915bff6116">LINECARDENTRY</a> structure. The 
<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a> function returns a 
<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">LINETRANSLATECAPS</a> structure. The <b>dwCardListOffset</b> member of this structure points to a list of 
<b>LINECARDENTRY</b> structures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallingCard</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITCallingCard</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallingCard</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d971d5ef-30d0-42a4-9a23-5b1388a0cb26">get_CardName</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the calling card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b452edbd-2c37-4f40-873b-24b4b60836bb">get_InternationalDialingRule</a>
</td>
<td align="left" width="63%">
Gets the international dialing rules for this calling card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97ad3528-ee84-4b61-9d08-55d3500432dd">get_LongDistanceDialingRule</a>
</td>
<td align="left" width="63%">
Gets the long distance dialing rules for this calling card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9eacfd2d-b137-4923-9cfa-139473ba8298">get_NumberOfDigits</a>
</td>
<td align="left" width="63%">
Gets the number of digits in the existing card number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0daa0058-759b-4f4c-8fb4-ce65e4fa9682">get_Options</a>
</td>
<td align="left" width="63%">
Gets the translation options for this address and card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75c37941-f950-4f86-be47-9aefe17995a5">get_PermanentCardID</a>
</td>
<td align="left" width="63%">
Gets the permanent calling card identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8539040-a988-4d96-8cf1-9ec8ff46a0a9">get_SameAreaDialingRule</a>
</td>
<td align="left" width="63%">
Gets the dialing rules for calls within the same area code.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/93f3cea1-70da-41f0-a8d5-692468a21695">ITAddressTranslation::EnumerateCallingCards</a>



<a href="https://msdn.microsoft.com/3033c584-1a7b-4bba-a8a2-2a2d59247689">ITAddressTranslation::get_CallingCards</a>



<a href="https://msdn.microsoft.com/8b2a4eaf-6c59-4d3b-839f-52915bff6116">LINECARDENTRY</a>



<a href="https://msdn.microsoft.com/9b4dcbe6-41e9-4b9c-9150-d0c7edef5a19">LINETRANSLATECAPS</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

