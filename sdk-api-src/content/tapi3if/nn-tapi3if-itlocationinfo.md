---
UID: NN:tapi3if.ITLocationInfo
title: ITLocationInfo
author: windows-sdk-content
description: The ITLocationInfo interface is used to get information related to the location of the calling party. This is the location information that is entered by using the Telephony applet under the Control Panel.
old-location: tapi3\itlocationinfo.htm
tech.root: tapi
ms.assetid: 0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITLocationInfo, ITLocationInfo interface [TAPI 2.2], ITLocationInfo interface [TAPI 2.2],described, _tapi3_itlocationinfo, tapi3.itlocationinfo, tapi3if/ITLocationInfo
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
 - ITLocationInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITLocationInfo interface


## -description


The 
<b>ITLocationInfo</b> interface is used to get information related to the location of the calling party. This is the location information that is entered by using the Telephony applet under the Control Panel.

An 
<b>ITLocationInfo</b> interface pointer is obtained by using 
<a href="https://msdn.microsoft.com/b286c738-1037-4a11-8c71-192b050d1502">ITAddressTranslation::EnumerateLocations</a> or 
<a href="https://msdn.microsoft.com/b18f7cb1-fcec-41eb-ac57-bf2d47f958e0">ITAddressTranslation::get_Locations</a>. There can be more than one location entries in the Telephony applet. If so, 
<b>EnumerateLocations</b> and 
<b>get_Locations</b> will return them all. However, only one of them is the current location, and TAPI uses that one as the address translation context when 
<a href="https://msdn.microsoft.com/14e51de8-33fd-4de0-bc1c-5f8085ea095c">ITAddressTranslation::TranslateAddress</a> is called.

The 
<b>ITLocationInfo</b> interface is a COM wrapper for the TAPI 2.<i>x</i>
<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a> structure.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITLocationInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITLocationInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITLocationInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49137921-7354-4080-8684-148beb919f01">get_CancelCallWaitingCode</a>
</td>
<td align="left" width="63%">
Gets the dial digits and modifier characters required to cancel call waiting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab8aee25-84b8-4913-876f-dd01bca5e3b0">get_CityCode</a>
</td>
<td align="left" width="63%">
Gets code for city or area.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ddd2e25-39ac-419b-9f99-85c6086f0377">get_CountryCode</a>
</td>
<td align="left" width="63%">
Gets country or region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c60e384b-ad0a-4e48-a337-b4ffad1b4891">get_CountryID</a>
</td>
<td align="left" width="63%">
Gets identifier for country or region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15e13c34-911f-4e4f-b7d9-f044bfb6c6d0">get_LocalAccessCode</a>
</td>
<td align="left" width="63%">
Gets local access code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bd86295-8240-477d-90aa-f3061666c5e6">get_LocationName</a>
</td>
<td align="left" width="63%">
Gets location name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c35e6a6a-3740-4595-90cd-709b4c9a42d1">get_LongDistanceAccessCode</a>
</td>
<td align="left" width="63%">
Gets code to access long distance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a53d7029-25a0-460c-97dd-c49355cc2ddc">get_Options</a>
</td>
<td align="left" width="63%">
Gets indicator of whether the current location supports pulse or tone dialing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dab6a20-6113-46ef-a5d2-855ac1befc1a">get_PermanentLocationID</a>
</td>
<td align="left" width="63%">
Gets permanent location identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7881a005-1bab-47a1-a657-31584d3f2713">get_PreferredCardID</a>
</td>
<td align="left" width="63%">
Gets preferred calling card identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45297e46-b1c8-45b0-bb16-8c5d5666bbd0">get_TollPrefixList</a>
</td>
<td align="left" width="63%">
Gets toll prefix list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/b286c738-1037-4a11-8c71-192b050d1502">ITAddressTranslation::EnumerateLocations</a>



<a href="https://msdn.microsoft.com/14e51de8-33fd-4de0-bc1c-5f8085ea095c">ITAddressTranslation::TranslateAddress</a>



<a href="https://msdn.microsoft.com/b18f7cb1-fcec-41eb-ac57-bf2d47f958e0">ITAddressTranslation::get_Locations</a>



<a href="https://msdn.microsoft.com/8b4357d8-6dc9-4fc8-b164-79675ac71870">LINELOCATIONENTRY</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>
 

 

