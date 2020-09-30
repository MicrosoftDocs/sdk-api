---
UID: NF:pla.IDataCollectorSetCollection.Remove
title: IDataCollectorSetCollection::Remove (pla.h)
description: Removes a data collector set from the collection.
helpviewer_keywords: ["IDataCollectorSetCollection interface [PLA]","Remove method","IDataCollectorSetCollection.Remove","IDataCollectorSetCollection::Remove","Remove","Remove method [PLA]","Remove method [PLA]","IDataCollectorSetCollection interface","base.idatacollectorsetcollection_remove","pla.idatacollectorsetcollection_remove","pla/IDataCollectorSetCollection::Remove"]
old-location: pla\idatacollectorsetcollection_remove.htm
tech.root: PLA
ms.assetid: 6200dac0-8817-4d59-9456-67921bcf15ae
ms.date: 12/05/2018
ms.keywords: IDataCollectorSetCollection interface [PLA],Remove method, IDataCollectorSetCollection.Remove, IDataCollectorSetCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],IDataCollectorSetCollection interface, base.idatacollectorsetcollection_remove, pla.idatacollectorsetcollection_remove, pla/IDataCollectorSetCollection::Remove
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDataCollectorSetCollection::Remove
 - pla/IDataCollectorSetCollection::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSetCollection.Remove
---

# IDataCollectorSetCollection::Remove


## -description

Removes a data collector set from the collection.

## -parameters

### -param set [in]

The zero-based index of the data collector set to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.

## -returns

Returns S_OK if successful.

## -remarks

If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a> to be removed.

Note that by removing the set from the collection, you are also deleting the set from the hard disk.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorsetcollection">IDataCollectorSetCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorsetcollection-add">IDataCollectorSetCollection::Add</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorsetcollection-clear">IDataCollectorSetCollection::Clear</a>