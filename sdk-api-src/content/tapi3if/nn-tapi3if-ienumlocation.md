---
UID: NN:tapi3if.IEnumLocation
title: IEnumLocation
author: windows-sdk-content
description: The IEnumLocation interface provides COM-standard enumeration methods for the ITLocationInfo interface. The ITAddressTranslation::EnumerateLocations method returns a pointer to IEnumLocation.
old-location: tapi3\ienumlocation.htm
tech.root: tapi
ms.assetid: fc8c235c-92ec-448f-bbea-c93192d36beb
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IEnumLocation, IEnumLocation interface [TAPI 2.2], IEnumLocation interface [TAPI 2.2],described, _tapi3_ienumlocation, tapi3.ienumlocation, tapi3if/IEnumLocation
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
 - IEnumLocation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumLocation interface


## -description


The 
<b>IEnumLocation</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/0f82a6f4-26a6-48dc-9bfa-a86edf1b6be4">ITLocationInfo</a> interface. The 
<a href="https://msdn.microsoft.com/b286c738-1037-4a11-8c71-192b050d1502">ITAddressTranslation::EnumerateLocations</a> method returns a pointer to 
<b>IEnumLocation</b>.

The 
<b>IEnumLocation</b> interface is hidden from Visual Basic and scripting languages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumLocation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumLocation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumLocation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c190f38-26f4-49a6-8dcb-49e61c09db43">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9fe8747-5c65-47fd-9e1a-2387971bdf15">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3933f0c-ae45-4749-916a-c2bc64ba41a0">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e365f95-5d84-449a-9ae2-eeb4ea269b0d">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

