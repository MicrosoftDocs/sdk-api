---
UID: NF:propidl.IPropertySetStorage.Delete
title: IPropertySetStorage::Delete (propidl.h)
description: The Delete method deletes one of the property sets contained in the property set storage object.
helpviewer_keywords: ["Delete","Delete method [Structured Storage]","Delete method [Structured Storage]","IPropertySetStorage interface","IPropertySetStorage [Strctd Stg]","Delete","IPropertySetStorage interface [Structured Storage]","Delete method","IPropertySetStorage.Delete","IPropertySetStorage::Delete","_stg_ipropertysetstorage_delete","propidl/IPropertySetStorage::Delete","stg.ipropertysetstorage_delete"]
old-location: stg\ipropertysetstorage_delete.htm
tech.root: Stg
ms.assetid: 5c65942f-b73b-48e5-a59e-4424708a084a
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Structured Storage], Delete method [Structured Storage],IPropertySetStorage interface, IPropertySetStorage [Strctd Stg],Delete, IPropertySetStorage interface [Structured Storage],Delete method, IPropertySetStorage.Delete, IPropertySetStorage::Delete, _stg_ipropertysetstorage_delete, propidl/IPropertySetStorage::Delete, stg.ipropertysetstorage_delete
req.header: propidl.h
req.include-header: Objbase.h
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
 - IPropertySetStorage::Delete
 - propidl/IPropertySetStorage::Delete
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
 - IPropertySetStorage.Delete
---

# IPropertySetStorage::Delete


## -description

The <b>Delete</b> method deletes one of the property sets contained in the property set storage object.

## -parameters

### -param rfmtid [in]

FMTID of the property set to be deleted.

## -returns

This method supports the standard return value E_UNEXPECTED, in addition to the following:

## -remarks

<b>IPropertySetStorage::Delete</b> deletes the property set specified by its FMTID. Specifying a property set that does not exist returns an error. Open substorages and streams(opened through one of the storage- or stream-valued properties) are put into the reverted state.

