---
UID: NF:pla.IDataCollectorCollection.Clear
title: IDataCollectorCollection::Clear (pla.h)
description: Removes all data collectors from the collection.
helpviewer_keywords: ["Clear","Clear method [PLA]","Clear method [PLA]","IDataCollectorCollection interface","IDataCollectorCollection interface [PLA]","Clear method","IDataCollectorCollection.Clear","IDataCollectorCollection::Clear","base.idatacollectorcollection_clear","pla.idatacollectorcollection_clear","pla/IDataCollectorCollection::Clear"]
old-location: pla\idatacollectorcollection_clear.htm
tech.root: PLA
ms.assetid: be0840dc-e19a-454e-bbea-6968c7284cc8
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [PLA], Clear method [PLA],IDataCollectorCollection interface, IDataCollectorCollection interface [PLA],Clear method, IDataCollectorCollection.Clear, IDataCollectorCollection::Clear, base.idatacollectorcollection_clear, pla.idatacollectorcollection_clear, pla/IDataCollectorCollection::Clear
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
 - IDataCollectorCollection::Clear
 - pla/IDataCollectorCollection::Clear
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
 - IDataCollectorCollection.Clear
---

# IDataCollectorCollection::Clear


## -description

Removes all data collectors from the collection.



## -returns

Returns S_OK if successful.

## -remarks

Note that by removing the collectors from the collection, you are also removing the collectors from the data collector set.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorcollection">IDataCollectorCollection</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-remove">IDataCollectorCollection::Remove</a>
