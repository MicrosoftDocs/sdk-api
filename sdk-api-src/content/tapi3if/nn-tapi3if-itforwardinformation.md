---
UID: NN:tapi3if.ITForwardInformation
title: ITForwardInformation
author: windows-sdk-content
description: The ITForwardInformation interface provides methods for setup and implementation of call forwarding.
old-location: tapi3\itforwardinformation.htm
old-project: tapi
ms.assetid: 0e06cd0b-b95b-4853-b883-53146be084f0
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITForwardInformation, ITForwardInformation interface [TAPI 2.2], ITForwardInformation interface [TAPI 2.2],described, _tapi3_itforwardinformation, tapi3.itforwardinformation, tapi3if/ITForwardInformation
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITForwardInformation
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITForwardInformation interface


## -description


The 
<b>ITForwardInformation</b> interface provides methods for setup and implementation of call forwarding. The forward information object is created by 
<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>. A pointer to an existing forward information object can be retrieved using 
<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITForwardInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITForwardInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITForwardInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Clears all forwarding information in this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fca5b5c-dd1e-4c8d-878a-99a7e3ec45f9">get_ForwardTypeCaller</a>
</td>
<td align="left" width="63%">
Gets the type of caller for a forwarding mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84a5737c-3bcd-4fdf-9a51-ef726fe71682">get_ForwardTypeDestination</a>
</td>
<td align="left" width="63%">
Gets the destination for a forwarding mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfd46f8b-6501-43ca-b3bd-35394526d5ce">get_NumRingsNoAnswer</a>
</td>
<td align="left" width="63%">
Retrieves the number of rings after which a no answer condition is assumed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02d3c558-585a-4dcc-873e-8465c1d2af64">GetForwardType</a>
</td>
<td align="left" width="63%">
Gets the forwarding mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad7b2746-cb97-406e-a328-efc051681aa6">put_NumRingsNoAnswer</a>
</td>
<td align="left" width="63%">
Sets the number of rings after which a no answer condition is assumed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f7972a8-c9b0-4033-8b00-a107a513ee66">SetForwardType</a>
</td>
<td align="left" width="63%">
Sets the forwarding mode.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">ITAddress::CreateForwardInfoObject</a>



<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">ITAddress::Forward</a>



<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">ITAddress::get_CurrentForwardInfo</a>



<a href="https://msdn.microsoft.com/25c99955-1a9d-49fa-9432-962e19296ad5">ITForwardInformation2</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>
 

 

