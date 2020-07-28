---
UID: NF:propidlbase.IPropertyStorage.Revert
title: IPropertyStorage::Revert (propidlbase.h)
description: The Revert method discards all changes to the named property set since it was last opened or discards changes that were last committed to the property set. This method has no effect on a direct-mode property set.
helpviewer_keywords: ["IPropertyStorage [Strctd Stg]","Revert","IPropertyStorage interface [Structured Storage]","Revert method","IPropertyStorage.Revert","IPropertyStorage::Revert","Revert","Revert method [Structured Storage]","Revert method [Structured Storage]","IPropertyStorage interface","_stg_ipropertystorage_revert","propidl/IPropertyStorage::Revert","stg.ipropertystorage_revert"]
old-location: stg\ipropertystorage_revert.htm
tech.root: Stg
ms.assetid: 31e0d3e7-8575-4788-b42e-606221cf5a4c
ms.date: 12/05/2018
ms.keywords: IPropertyStorage [Strctd Stg],Revert, IPropertyStorage interface [Structured Storage],Revert method, IPropertyStorage.Revert, IPropertyStorage::Revert, Revert, Revert method [Structured Storage], Revert method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_revert, propidl/IPropertyStorage::Revert, stg.ipropertystorage_revert
f1_keywords:
- propidlbase/IPropertyStorage.Revert
dev_langs:
- c++
req.header: propidlbase.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IPropertyStorage.Revert
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStorage::Revert


## -description


The <b>Revert</b> method discards all changes to the named property set since it was last opened or discards changes that were last committed to the property set. This method has no effect on a direct-mode property set.


## -parameters






## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



For transacted-mode property sets, this method discards all changes that have been made in this property set since the set was opened or since the time it was last committed, (whichever is later). After this operation, any existing storage- or stream-valued properties that have been opened from the property set being reverted are no longer valid and cannot be used. The error STG_E_REVERTED will be returned on all calls, except those to <b>Release</b>, using these streams or storages.

For direct-mode property sets, this request is ignored and returns S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-commit">IPropertyStorage::Commit</a>
 

 

