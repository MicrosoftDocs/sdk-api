---
UID: NF:pla.ITraceDataProviderCollection.get__NewEnum
title: ITraceDataProviderCollection::get__NewEnum (pla.h)
description: Retrieves an interface to the enumeration. (ITraceDataProviderCollection.get__NewEnum)
helpviewer_keywords: ["ITraceDataProviderCollection interface [PLA]","_NewEnum property","ITraceDataProviderCollection._NewEnum","ITraceDataProviderCollection.get__NewEnum","ITraceDataProviderCollection::_NewEnum","ITraceDataProviderCollection::get__NewEnum","_NewEnum property [PLA]","_NewEnum property [PLA]","ITraceDataProviderCollection interface","get__NewEnum","pla.itracedataprovidercollection__newenum","pla/ITraceDataProviderCollection::_NewEnum","pla/ITraceDataProviderCollection::get__NewEnum"]
old-location: pla\itracedataprovidercollection__newenum.htm
tech.root: PLA
ms.assetid: cd80839a-0cf0-4553-819e-7a8be830b9fa
ms.date: 12/05/2018
ms.keywords: ITraceDataProviderCollection interface [PLA],_NewEnum property, ITraceDataProviderCollection._NewEnum, ITraceDataProviderCollection.get__NewEnum, ITraceDataProviderCollection::_NewEnum, ITraceDataProviderCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],ITraceDataProviderCollection interface, get__NewEnum, pla.itracedataprovidercollection__newenum, pla/ITraceDataProviderCollection::_NewEnum, pla/ITraceDataProviderCollection::get__NewEnum
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
 - ITraceDataProviderCollection::get__NewEnum
 - pla/ITraceDataProviderCollection::get__NewEnum
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
 - ITraceDataProviderCollection._NewEnum
 - ITraceDataProviderCollection.get__NewEnum
---

# ITraceDataProviderCollection::get__NewEnum


## -description

Retrieves an interface to the enumeration.

This property is read-only.

## -parameters

## -remarks

 C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a> interface, use the <b>punkVal</b> member of the variant.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>
