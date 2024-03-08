---
UID: NF:pla.IFolderActionCollection.get__NewEnum
title: IFolderActionCollection::get__NewEnum (pla.h)
description: Retrieves an interface to the enumeration. (IFolderActionCollection.get__NewEnum)
helpviewer_keywords: ["IFolderActionCollection interface [PLA]","_NewEnum property","IFolderActionCollection._NewEnum","IFolderActionCollection.get__NewEnum","IFolderActionCollection::_NewEnum","IFolderActionCollection::get__NewEnum","_NewEnum property [PLA]","_NewEnum property [PLA]","IFolderActionCollection interface","base.ifolderactioncollection__newenum","get__NewEnum","pla.ifolderactioncollection__newenum","pla/IFolderActionCollection::_NewEnum","pla/IFolderActionCollection::get__NewEnum"]
old-location: pla\ifolderactioncollection__newenum.htm
tech.root: PLA
ms.assetid: 92b13b4f-31bd-42c7-9aed-02cef9ca38f3
ms.date: 12/05/2018
ms.keywords: IFolderActionCollection interface [PLA],_NewEnum property, IFolderActionCollection._NewEnum, IFolderActionCollection.get__NewEnum, IFolderActionCollection::_NewEnum, IFolderActionCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IFolderActionCollection interface, base.ifolderactioncollection__newenum, get__NewEnum, pla.ifolderactioncollection__newenum, pla/IFolderActionCollection::_NewEnum, pla/IFolderActionCollection::get__NewEnum
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
 - IFolderActionCollection::get__NewEnum
 - pla/IFolderActionCollection::get__NewEnum
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
 - IFolderActionCollection._NewEnum
 - IFolderActionCollection.get__NewEnum
---

# IFolderActionCollection::get__NewEnum


## -description

Retrieves an interface to the enumeration.

This property is read-only.

## -parameters

## -remarks

C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="/previous-versions/windows/desktop/api/pla/nn-pla-ifolderaction">IFolderAction</a> interface, use the <b>punkVal</b> member of the variant.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ifolderactioncollection">IFolderActionCollection</a>
