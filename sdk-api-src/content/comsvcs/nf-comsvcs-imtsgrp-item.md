---
UID: NF:comsvcs.IMtsGrp.Item
title: IMtsGrp::Item (comsvcs.h)
description: Retrieves the IUnknown pointer for the specified package.
helpviewer_keywords: ["IMtsGrp interface [COM+]","Item method","IMtsGrp.Item","IMtsGrp::Item","Item","Item method [COM+]","Item method [COM+]","IMtsGrp interface","_dtc_IMtsGrp_Item","comsvcs/IMtsGrp::Item","cos.imtsgrp_item"]
old-location: cos\imtsgrp_item.htm
tech.root: cos
ms.assetid: 6360f38d-43e2-4b78-a9f5-9a525d4c596a
ms.date: 12/05/2018
ms.keywords: IMtsGrp interface [COM+],Item method, IMtsGrp.Item, IMtsGrp::Item, Item, Item method [COM+], Item method [COM+],IMtsGrp interface, _dtc_IMtsGrp_Item, comsvcs/IMtsGrp::Item, cos.imtsgrp_item
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IMtsGrp::Item
 - comsvcs/IMtsGrp::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMtsGrp.Item
---

# IMtsGrp::Item


## -description

Retrieves the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer for the specified package.

## -parameters

### -param lIndex [in]

The index containing running packages.

### -param ppUnkDispatcher [out]

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer, which can be used to access <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsevents">IMtsEvents</a>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsgrp">IMtsGrp</a>