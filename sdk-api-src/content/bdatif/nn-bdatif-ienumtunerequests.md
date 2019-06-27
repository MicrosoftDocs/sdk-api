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
f1_keywords: 
 - "bdatif/IEnumTuneRequests"
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
ms.custom: 19H1
---

# IEnumTuneRequests interface


## -description



The <b>IEnumTuneRequests</b> interface provides access to a collection of tune requests returned from a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getservices">IGuideData::GetServices</a>. This collection of tune requests represents all the services available in the tuning space.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTuneRequests</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTuneRequests</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-ienumtunerequests-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-ienumtunerequests-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next item or items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-ienumtunerequests-reset">Reset</a>
</td>
<td align="left" width="63%">
Sets the enumerator to the first item in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-ienumtunerequests-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified number of items.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumTuneRequests)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

