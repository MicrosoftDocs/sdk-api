---
UID: NF:pla.IValueMap.get__NewEnum
title: IValueMap::get__NewEnum (pla.h)
description: Retrieves an interface to the enumeration. (IValueMap.get__NewEnum)
helpviewer_keywords: ["IValueMap interface [PLA]","_NewEnum property","IValueMap._NewEnum","IValueMap.get__NewEnum","IValueMap::_NewEnum","IValueMap::get__NewEnum","_NewEnum property [PLA]","_NewEnum property [PLA]","IValueMap interface","get__NewEnum","pla.ivaluemap__newenum","pla/IValueMap::_NewEnum","pla/IValueMap::get__NewEnum"]
old-location: pla\ivaluemap__newenum.htm
tech.root: PLA
ms.assetid: 1d40104c-c0a4-41d2-8427-364c37b52e02
ms.date: 12/05/2018
ms.keywords: IValueMap interface [PLA],_NewEnum property, IValueMap._NewEnum, IValueMap.get__NewEnum, IValueMap::_NewEnum, IValueMap::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IValueMap interface, get__NewEnum, pla.ivaluemap__newenum, pla/IValueMap::_NewEnum, pla/IValueMap::get__NewEnum
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
 - IValueMap::get__NewEnum
 - pla/IValueMap::get__NewEnum
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
 - IValueMap._NewEnum
 - IValueMap.get__NewEnum
---

# IValueMap::get__NewEnum


## -description

Retrieves an interface to the enumeration.

This property is read-only.

## -parameters

## -remarks

 C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemapitem">IValueMapItem</a> interface, use the <b>punkVal</b> member of the variant.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ivaluemap">IValueMap</a>
