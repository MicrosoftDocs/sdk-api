---
UID: NN:tapi3if.ITForwardInformation2
title: ITForwardInformation2
author: windows-sdk-content
description: The ITForwardInformation2 interface exposes methods that provide additional methods for the control of forwarding information. See ITForwardInformation for the basic forwarding control methods.
old-location: tapi3\itforwardinformation2.htm
tech.root: tapi
ms.assetid: 25c99955-1a9d-49fa-9432-962e19296ad5
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITForwardInformation2, ITForwardInformation2 interface [TAPI 2.2], ITForwardInformation2 interface [TAPI 2.2],described, _tapi3_itforwardinformation2, tapi3.itforwardinformation2, tapi3if/ITForwardInformation2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3if.h
req.include-header: 
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
 - ITForwardInformation2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITForwardInformation2 interface


## -description


The 
<b>ITForwardInformation2</b> interface exposes methods that provide additional methods for the control of forwarding information. See 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a> for the basic forwarding control methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITForwardInformation2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITForwardInformation2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITForwardInformation2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/030d2b44-0c1d-488b-8cd9-e68ad6d26c6e">get_ForwardTypeCallerAddressType</a>
</td>
<td align="left" width="63%">
Gets the destination address type for a given forwarding type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de40538a-e2ba-49ec-bde6-6803da6515da">get_ForwardTypeDestinationAddressType</a>
</td>
<td align="left" width="63%">
Gets the caller address type for a given forwarding type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3142217-d3fa-4e0b-ad3b-65a0557ce951">GetForwardType2</a>
</td>
<td align="left" width="63%">
Gets the current forwarding mode, specified by caller address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/774b91e8-b7f9-47b5-bbd9-025b03429b14">SetForwardType2</a>
</td>
<td align="left" width="63%">
Sets the current forwarding mode, specified by caller address.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>



<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

