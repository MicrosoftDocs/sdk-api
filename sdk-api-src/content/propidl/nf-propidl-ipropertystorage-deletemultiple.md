---
UID: NF:propidl.IPropertyStorage.DeleteMultiple
title: IPropertyStorage::DeleteMultiple (propidl.h)
description: The IPropertyStorage::DeleteMultiple method deletes as many of the indicated properties as exist in this property set. 
helpviewer_keywords: ["DeleteMultiple","DeleteMultiple method [Structured Storage]","DeleteMultiple method [Structured Storage]","IPropertyStorage interface","IPropertyStorage [Strctd Stg]","DeleteMultiple","IPropertyStorage interface [Structured Storage]","DeleteMultiple method","IPropertyStorage.DeleteMultiple","IPropertyStorage::DeleteMultiple","_stg_ipropertystorage_deletemultiple","propidl/IPropertyStorage::DeleteMultiple","stg.ipropertystorage_deletemultiple"]
old-location: stg\ipropertystorage_deletemultiple.htm
tech.root: Stg
ms.assetid: 95c218f1-2bf7-4946-ae9c-934e5916395a
ms.date: 08/02/2022
ms.keywords: DeleteMultiple, DeleteMultiple method [Structured Storage], DeleteMultiple method [Structured Storage],IPropertyStorage interface, IPropertyStorage [Strctd Stg],DeleteMultiple, IPropertyStorage interface [Structured Storage],DeleteMultiple method, IPropertyStorage.DeleteMultiple, IPropertyStorage::DeleteMultiple, _stg_ipropertystorage_deletemultiple, propidl/IPropertyStorage::DeleteMultiple, stg.ipropertystorage_deletemultiple
req.header: propidl.h
req.include-header: Objbase.h, Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyStorage::DeleteMultiple
 - propidl/IPropertyStorage::DeleteMultiple
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertyStorage.DeleteMultiple
---

# IPropertyStorage::DeleteMultiple


## -description

The <b>DeleteMultiple</b> method deletes as many of the indicated properties as exist in this property set.

## -parameters

### -param cpspec [in]

The numerical count of properties to be deleted. The value of this parameter can  legally be set to zero, however that defeats the purpose of the method as no properties are thereby deleted, regardless of the value set in <i>rgpspec</i>.

### -param rgpspec [in]

Properties to be deleted. A mixture of property identifiers and string-named properties is permitted. There may be duplicates, and there is no requirement that properties be specified in any order.

## -returns

This method supports the standard return value E_UNEXPECTED, in addition to the following:

## -remarks

<b>IPropertyStorage::DeleteMultiple</b> must delete as many of the indicated properties as are in the current property set. If a deletion of a stream- or storage-valued property occurs while that property is open, the deletion will succeed and place the previously returned 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> or 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer in the reverted state.
