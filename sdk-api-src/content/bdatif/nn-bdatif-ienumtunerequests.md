---
UID: NN:bdatif.IEnumTuneRequests
title: IEnumTuneRequests (bdatif.h)
description: The IEnumTuneRequests interface provides access to a collection of tune requests returned from a call to IGuideData::GetServices. This collection of tune requests represents all the services available in the tuning space.
helpviewer_keywords: ["IEnumTuneRequests","IEnumTuneRequests interface [Microsoft TV Technologies]","IEnumTuneRequests interface [Microsoft TV Technologies]","described","IEnumTuneRequestsInterface","bdatif/IEnumTuneRequests","mstv.ienumtunerequests"]
old-location: mstv\ienumtunerequests.htm
tech.root: mstv
ms.assetid: 5ad872be-4408-4069-80db-ae73b2127b91
ms.date: 12/05/2018
ms.keywords: IEnumTuneRequests, IEnumTuneRequests interface [Microsoft TV Technologies], IEnumTuneRequests interface [Microsoft TV Technologies],described, IEnumTuneRequestsInterface, bdatif/IEnumTuneRequests, mstv.ienumtunerequests
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumTuneRequests
 - bdatif/IEnumTuneRequests
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - IEnumTuneRequests
---

# IEnumTuneRequests interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IEnumTuneRequests</b> interface provides access to a collection of tune requests returned from a call to <a href="/previous-versions/windows/desktop/api/bdatif/nf-bdatif-iguidedata-getservices">IGuideData::GetServices</a>. This collection of tune requests represents all the services available in the tuning space.

## -inheritance

The <b>IEnumTuneRequests</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTuneRequests</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumTuneRequests)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
