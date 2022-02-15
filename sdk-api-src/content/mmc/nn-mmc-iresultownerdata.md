---
UID: NN:mmc.IResultOwnerData
title: IResultOwnerData (mmc.h)
description: The IResultOwnerData interface supports the use of virtual lists, which are list-view controls that have the LVS_OWNERDATA style set.
helpviewer_keywords: ["IResultOwnerData","IResultOwnerData interface [MMC]","IResultOwnerData interface [MMC]","described","_slate_iresultownerdata","mmc.iresultownerdata","mmc/IResultOwnerData"]
old-location: mmc\iresultownerdata.htm
tech.root: mmc
ms.assetid: 184f3783-9000-45aa-867b-580800b560b3
ms.date: 12/05/2018
ms.keywords: IResultOwnerData, IResultOwnerData interface [MMC], IResultOwnerData interface [MMC],described, _slate_iresultownerdata, mmc.iresultownerdata, mmc/IResultOwnerData
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IResultOwnerData
 - mmc/IResultOwnerData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultOwnerData
---

# IResultOwnerData interface


## -description

The 
<b>IResultOwnerData</b> interface supports the use of virtual lists, which are list-view controls that have the LVS_OWNERDATA style set. The methods of this interface are applicable only to virtual lists. This is an optional interface and snap-ins can implement it for enhanced virtual list performance and functionality.

## -inheritance

The <b>IResultOwnerData</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultOwnerData</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo">IComponent::GetDisplayInfo</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a>



<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-setitemcount">IResultData::SetItemCount</a>



<a href="/previous-versions/windows/desktop/mmc/owner-data-virtual-lists">Owner Data/Virtual Lists</a>



<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a>
