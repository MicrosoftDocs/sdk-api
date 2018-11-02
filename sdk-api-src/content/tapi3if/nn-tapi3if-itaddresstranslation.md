---
UID: NN:tapi3if.ITAddressTranslation
title: ITAddressTranslation
author: windows-sdk-content
description: The ITAddressTranslation interface provides methods that allow translation of a calling address into a different format. For example, an application may need to translate an address from canonical to dialable prior to making a call.
old-location: tapi3\itaddresstranslation.htm
tech.root: tapi
ms.assetid: e1cd88f1-1ed7-4e7f-a745-9a9c4af69317
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITAddressTranslation, ITAddressTranslation interface [TAPI 2.2], ITAddressTranslation interface [TAPI 2.2],described, _tapi3_itaddresstranslation, tapi3.itaddresstranslation, tapi3if/ITAddressTranslation
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
 - ITAddressTranslation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressTranslation interface


## -description


The 
<b>ITAddressTranslation</b> interface provides methods that allow translation of a calling address into a different format. For example, an application may need to translate an address from canonical to dialable prior to making a call.

The most common use of this interface is to obtain the <i>pDestAddress</i> string needed for 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>. The addresses to be translated are mainly phone numbers in canonical format.

The 
<b>ITAddressTranslation</b> interface is exposed on the 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>. A pointer can be obtained by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>.

For additional information, see 
<a href="https://msdn.microsoft.com/en-us/library/ms728172(v=VS.85).aspx">Address Translation</a> and 
<a href="https://msdn.microsoft.com/en-us/library/ms726017(v=VS.85).aspx">Dialable Addresses</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressTranslation</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITAddressTranslation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddressTranslation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93f3cea1-70da-41f0-a8d5-692468a21695">EnumerateCallingCards</a>
</td>
<td align="left" width="63%">
Enumerates calling cards associated with the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b286c738-1037-4a11-8c71-192b050d1502">EnumerateLocations</a>
</td>
<td align="left" width="63%">
Enumerates the currently available address locations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3033c584-1a7b-4bba-a8a2-2a2d59247689">get_CallingCards</a>
</td>
<td align="left" width="63%">
Creates a collection of calling cards associated with the address. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b18f7cb1-fcec-41eb-ac57-bf2d47f958e0">get_Locations</a>
</td>
<td align="left" width="63%">
Creates a collection of currently available address locations. This method is provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14e51de8-33fd-4de0-bc1c-5f8085ea095c">TranslateAddress</a>
</td>
<td align="left" width="63%">
Creates the address translation information interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe744658-b5a7-4d22-bf8b-9c669be3da1e">TranslateDialog</a>
</td>
<td align="left" width="63%">
Invokes the control panel's telephony applet.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/en-us/library/ms728172(v=VS.85).aspx">Address Translation</a>



<a href="https://msdn.microsoft.com/en-us/library/ms726017(v=VS.85).aspx">Dialable Addresses</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>



<a href="https://msdn.microsoft.com/77437b06-fb02-44b5-8642-b3de700853ef">lineGetTranslateCaps</a>



<a href="https://msdn.microsoft.com/0347d526-9596-4b42-8075-07318bf39634">lineTranslateAddress</a>
 

 

