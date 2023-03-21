---
UID: NF:pla.IDataCollectorSetCollection.get__NewEnum
title: IDataCollectorSetCollection::get__NewEnum (pla.h)
description: Retrieves an interface to the enumeration. (IDataCollectorSetCollection.get__NewEnum)
helpviewer_keywords: ["IDataCollectorSetCollection interface [PLA]","_NewEnum property","IDataCollectorSetCollection._NewEnum","IDataCollectorSetCollection.get__NewEnum","IDataCollectorSetCollection::_NewEnum","IDataCollectorSetCollection::get__NewEnum","_NewEnum property [PLA]","_NewEnum property [PLA]","IDataCollectorSetCollection interface","get__NewEnum","pla.idatacollectorsetcollection__newenum","pla/IDataCollectorSetCollection::_NewEnum","pla/IDataCollectorSetCollection::get__NewEnum"]
old-location: pla\idatacollectorsetcollection__newenum.htm
tech.root: PLA
ms.assetid: f875038d-8b66-44b2-b28e-211f08a691ec
ms.date: 12/05/2018
ms.keywords: IDataCollectorSetCollection interface [PLA],_NewEnum property, IDataCollectorSetCollection._NewEnum, IDataCollectorSetCollection.get__NewEnum, IDataCollectorSetCollection::_NewEnum, IDataCollectorSetCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IDataCollectorSetCollection interface, get__NewEnum, pla.idatacollectorsetcollection__newenum, pla/IDataCollectorSetCollection::_NewEnum, pla/IDataCollectorSetCollection::get__NewEnum
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
 - IDataCollectorSetCollection::get__NewEnum
 - pla/IDataCollectorSetCollection::get__NewEnum
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
 - IDataCollectorSetCollection._NewEnum
 - IDataCollectorSetCollection.get__NewEnum
---

# IDataCollectorSetCollection::get__NewEnum


## -description

Retrieves an interface to the enumeration.

This property is read-only.

## -parameters

## -remarks

C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN.  To query for the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a> interface, use the <b>punkVal</b> member of the variant.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorsetcollection">IDataCollectorSetCollection</a>
