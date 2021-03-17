---
UID: NF:pla.IDataCollectorCollection.Remove
title: IDataCollectorCollection::Remove (pla.h)
description: Removes a data collector from the collection.
helpviewer_keywords: ["IDataCollectorCollection interface [PLA]","Remove method","IDataCollectorCollection.Remove","IDataCollectorCollection::Remove","Remove","Remove method [PLA]","Remove method [PLA]","IDataCollectorCollection interface","base.idatacollectorcollection_remove","pla.idatacollectorcollection_remove","pla/IDataCollectorCollection::Remove"]
old-location: pla\idatacollectorcollection_remove.htm
tech.root: PLA
ms.assetid: 7f5a6d20-d65a-477b-8886-8536315bc36e
ms.date: 12/05/2018
ms.keywords: IDataCollectorCollection interface [PLA],Remove method, IDataCollectorCollection.Remove, IDataCollectorCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],IDataCollectorCollection interface, base.idatacollectorcollection_remove, pla.idatacollectorcollection_remove, pla/IDataCollectorCollection::Remove
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
 - IDataCollectorCollection::Remove
 - pla/IDataCollectorCollection::Remove
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
 - IDataCollectorCollection.Remove
---

# IDataCollectorCollection::Remove


## -description

Removes a data collector from the collection.

## -parameters

### -param collector [in]

The zero-based index of the data collector to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.

## -returns

Returns S_OK if successful.

## -remarks

If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> to be removed.

Note that by removing the collector from the collection, you are also removing the collector from the data collector set.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorcollection">IDataCollectorCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-add">IDataCollectorCollection::Add</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-clear">IDataCollectorCollection::Clear</a>