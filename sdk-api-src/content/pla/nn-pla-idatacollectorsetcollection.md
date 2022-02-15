---
UID: NN:pla.IDataCollectorSetCollection
title: IDataCollectorSetCollection (pla.h)
description: Manages a collection of DataCollectorSet objects.To get this interface, call the CoCreateInstance function, passing __uuidof(DataCollectorSetCollection) as the class identifier and __uuidof(IDataCollectorSetCollection) as the interface identifier.Then, to populate the collection, call the IDataCollectorSetCollection::GetDataCollectorSets method.
helpviewer_keywords: ["IDataCollectorSetCollection","IDataCollectorSetCollection interface [PLA]","IDataCollectorSetCollection interface [PLA]","described","base.idatacollectorsetcollection","pla.idatacollectorsetcollection","pla/IDataCollectorSetCollection"]
old-location: pla\idatacollectorsetcollection.htm
tech.root: PLA
ms.assetid: 5f4cc411-1efb-4f70-a677-3c20d95f0c53
ms.date: 12/05/2018
ms.keywords: IDataCollectorSetCollection, IDataCollectorSetCollection interface [PLA], IDataCollectorSetCollection interface [PLA],described, base.idatacollectorsetcollection, pla.idatacollectorsetcollection, pla/IDataCollectorSetCollection
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
 - IDataCollectorSetCollection
 - pla/IDataCollectorSetCollection
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
 - IDataCollectorSetCollection
---

# IDataCollectorSetCollection interface


## -description

Manages a collection of <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">DataCollectorSet</a> objects.

To get this interface, call the <b>CoCreateInstance</b> function, passing __uuidof(DataCollectorSetCollection) as the class identifier and __uuidof(<b>IDataCollectorSetCollection</b>) as the interface identifier.

Then, to populate the collection, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorsetcollection-getdatacollectorsets">IDataCollectorSetCollection::GetDataCollectorSets</a> method.

## -inheritance

The <b>IDataCollectorSetCollection</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDataCollectorSetCollection</b> also has these types of members:

## -remarks

To create the object from a script, use the Pla.DataCollectorSetCollection program identifier.
