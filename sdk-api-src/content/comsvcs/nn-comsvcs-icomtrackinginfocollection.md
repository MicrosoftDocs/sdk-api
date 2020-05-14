---
UID: NN:comsvcs.IComTrackingInfoCollection
title: IComTrackingInfoCollection (comsvcs.h)
description: Retrieves information about a tracking information collection.helpviewer_keywords: ["IComTrackingInfoCollection","IComTrackingInfoCollection interface [COM+]","IComTrackingInfoCollection interface [COM+]","described","_dtc_IComTrackingInfoCollection","comsvcs/IComTrackingInfoCollection","cos.icomtrackinginfocollection"]
old-location: cos\icomtrackinginfocollection.htm
tech.root: cossdk
ms.assetid: 7caa0fd3-a42c-43ea-849d-aa2c4ed1c628
ms.date: 12/05/2018
ms.keywords: IComTrackingInfoCollection, IComTrackingInfoCollection interface [COM+], IComTrackingInfoCollection interface [COM+],described, _dtc_IComTrackingInfoCollection, comsvcs/IComTrackingInfoCollection, cos.icomtrackinginfocollection
f1_keywords:
- comsvcs/IComTrackingInfoCollection
dev_langs:
- c++
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- ComSvcs.h
api_name:
- IComTrackingInfoCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComTrackingInfoCollection interface


## -description


Retrieves information about a tracking information collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComTrackingInfoCollection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComTrackingInfoCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComTrackingInfoCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomtrackinginfocollection-count">Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of objects in a tracking information collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomtrackinginfocollection-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves the specified interface from a specified member of a tracking information collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-icomtrackinginfocollection-type">Type</a>
</td>
<td align="left" width="63%">
Retrieves the type of a tracking information collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--tracking">COM+ Tracking</a>
 

 

