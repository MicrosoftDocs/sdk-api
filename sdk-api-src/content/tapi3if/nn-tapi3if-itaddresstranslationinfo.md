---
UID: NN:tapi3if.ITAddressTranslationInfo
title: ITAddressTranslationInfo
author: windows-sdk-content
description: Used to determine the address translation data.
old-location: tapi3\itaddresstranslationinfo.htm
tech.root: tapi
ms.assetid: b59454a0-315f-4160-b969-d930c13bb4de
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAddressTranslationInfo, ITAddressTranslationInfo interface [TAPI 2.2], ITAddressTranslationInfo interface [TAPI 2.2],described, _tapi3_itaddresstranslationinfo, tapi3.itaddresstranslationinfo, tapi3if/ITAddressTranslationInfo
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
 - ITAddressTranslationInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressTranslationInfo interface


## -description


The 
<b>ITAddressTranslationInfo</b> interface is used to determine the address translation data. To obtain a pointer to it, call 
<a href="https://msdn.microsoft.com/14e51de8-33fd-4de0-bc1c-5f8085ea095c">ITAddressTranslation::TranslateAddress</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressTranslationInfo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITAddressTranslationInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddressTranslationInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02b19558-d7cb-4c77-977b-9810468ff145">get_CurrentCountryCode</a>
</td>
<td align="left" width="63%">
Gets the current country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29880773-ce19-489f-81d8-d2c91779350f">get_DestinationCountryCode</a>
</td>
<td align="left" width="63%">
Gets the country/region code for the call destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76177de9-eab2-4a86-ac25-29b78606b854">get_DialableString</a>
</td>
<td align="left" width="63%">
Gets a string that contains a number to be dialed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c88474ee-5a7e-4966-8dc2-5f839069b2d2">get_DisplayableString</a>
</td>
<td align="left" width="63%">
Gets a string that contains a displayable version of the number to be dialed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca6ac2c9-612d-4294-ab49-7c0278519a24">get_TranslationResults</a>
</td>
<td align="left" width="63%">
Gets the translated dialed number calling address.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>



<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a>
 

 

