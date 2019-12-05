---
UID: NF:objidl.IStorage.SetClass
title: IStorage::SetClass (objidl.h)
description: The SetClass method assigns the specified class identifier (CLSID) to this storage object.
old-location: stg\istorage_setclass.htm
tech.root: Stg
ms.assetid: 02ab2708-fc8b-4941-939a-a819cf823108
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],SetClass method, IStorage.SetClass, IStorage::SetClass, SetClass, SetClass method [Structured Storage], SetClass method [Structured Storage],IStorage interface, _stg_istorage_setclass, objidl/IStorage::SetClass, stg.istorage_setclass
ms.topic: method
f1_keywords:
- objidl/IStorage.SetClass
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
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
- IStorage.SetClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorage::SetClass


## -description


The <b>SetClass</b> method assigns the specified class identifier (CLSID) to this storage object.


## -parameters




### -param clsid [in]

The CLSID that is to be associated with the storage object.


## -returns



This method can return one of these values.




## -remarks



When first created, a storage object has an associated CLSID of CLSID_NULL. Call <b>SetClass</b> to assign a CLSID to the storage object.

Call the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a> method to retrieve the current CLSID of a storage object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-stat">IStorage::Stat</a>
 

 

