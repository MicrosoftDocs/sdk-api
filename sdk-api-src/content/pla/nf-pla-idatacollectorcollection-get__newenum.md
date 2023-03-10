---
UID: NF:pla.IDataCollectorCollection.get__NewEnum
title: IDataCollectorCollection::get__NewEnum (pla.h)
description: Retrieves an interface to the enumeration. (IDataCollectorCollection.get__NewEnum)
helpviewer_keywords: ["IDataCollectorCollection interface [PLA]","_NewEnum property","IDataCollectorCollection._NewEnum","IDataCollectorCollection.get__NewEnum","IDataCollectorCollection::_NewEnum","IDataCollectorCollection::get__NewEnum","_NewEnum property [PLA]","_NewEnum property [PLA]","IDataCollectorCollection interface","get__NewEnum","pla.idatacollectorcollection__newenum","pla/IDataCollectorCollection::_NewEnum","pla/IDataCollectorCollection::get__NewEnum"]
old-location: pla\idatacollectorcollection__newenum.htm
tech.root: PLA
ms.assetid: 05b97d37-9ccc-4856-a71a-77dd99eab8c2
ms.date: 12/05/2018
ms.keywords: IDataCollectorCollection interface [PLA],_NewEnum property, IDataCollectorCollection._NewEnum, IDataCollectorCollection.get__NewEnum, IDataCollectorCollection::_NewEnum, IDataCollectorCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IDataCollectorCollection interface, get__NewEnum, pla.idatacollectorcollection__newenum, pla/IDataCollectorCollection::_NewEnum, pla/IDataCollectorCollection::get__NewEnum
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
 - IDataCollectorCollection::get__NewEnum
 - pla/IDataCollectorCollection::get__NewEnum
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
 - IDataCollectorCollection._NewEnum
 - IDataCollectorCollection.get__NewEnum
---

# IDataCollectorCollection::get__NewEnum


## -description

Retrieves an interface to the enumeration.

This property is read-only.

## -parameters

## -remarks

C++ programmers use this property.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> interface, use the <b>punkVal</b> member of the variant.

The enumeration is a snapshot of the collection at the time of the call.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorcollection">IDataCollectorCollection</a>
