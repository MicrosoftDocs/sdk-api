---
UID: NN:tapi3if.IEnumAddress
title: IEnumAddress
author: windows-sdk-content
description: The IEnumAddress interface provides COM-standard enumeration methods for the ITAddress interface. The ITTAPI::EnumerateAddresses and ITAgentHandler::EnumerateUsableAddresses methods return a pointer to IEnumAddress.
old-location: tapi3\ienumaddress.htm
old-project: tapi
ms.assetid: bfe9f12e-ceb7-4120-8193-70feb2bc7c85
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: IEnumAddress, IEnumAddress interface [TAPI 2.2], IEnumAddress interface [TAPI 2.2],described, _tapi3_ienumaddress, tapi3.ienumaddress, tapi3if/IEnumAddress
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
 - IEnumAddress
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumAddress interface


## -description


The 
<b>IEnumAddress</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface. The 
<a href="https://msdn.microsoft.com/b40a2071-24bf-470c-bfba-de23317e8652">ITTAPI::EnumerateAddresses</a> and 
<a href="https://msdn.microsoft.com/9821b073-c64b-4f2b-b771-6bf027f9aa70">ITAgentHandler::EnumerateUsableAddresses</a> methods return a pointer to 
<b>IEnumAddress</b>.

The 
<b>IEnumAddress</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumAddress</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>
 

 

