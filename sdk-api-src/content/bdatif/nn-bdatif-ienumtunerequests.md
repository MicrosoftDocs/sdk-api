---
UID: NN:bdatif.IEnumTuneRequests
title: IEnumTuneRequests (bdatif.h)
author: windows-sdk-content
description: The IEnumTuneRequests interface provides access to a collection of tune requests returned from a call to IGuideData::GetServices. This collection of tune requests represents all the services available in the tuning space.
old-location: mstv\ienumtunerequests.htm
tech.root: mstv
ms.assetid: 5ad872be-4408-4069-80db-ae73b2127b91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumTuneRequests, IEnumTuneRequests interface [Microsoft TV Technologies], IEnumTuneRequests interface [Microsoft TV Technologies],described, IEnumTuneRequestsInterface, bdatif/IEnumTuneRequests, mstv.ienumtunerequests
ms.topic: interface
req.header: bdatif.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - IEnumTuneRequests
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumTuneRequests interface


## -description



The <b>IEnumTuneRequests</b> interface provides access to a collection of tune requests returned from a call to <a href="https://msdn.microsoft.com/a3c08812-ed56-440e-a88d-80e20a681695">IGuideData::GetServices</a>. This collection of tune requests represents all the services available in the tuning space.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTuneRequests</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTuneRequests</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTuneRequests</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9910d646-c98e-479a-8abd-5d5427ef11b5">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb846bdb-f0ce-44f7-8d15-608c21e095c1">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next item or items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb06a6b3-83a6-4deb-8394-1c17cf97c1b2">Reset</a>
</td>
<td align="left" width="63%">
Sets the enumerator to the first item in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43ed5c7e-2d31-417e-9d87-c3100e5096d0">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of items.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumTuneRequests)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

