---
UID: NF:objidl.IStorage.OpenStorage
title: IStorage::OpenStorage (objidl.h)
description: Opens an existing storage object with the specified name in the specified access mode.
old-location: stg\istorage_openstorage.htm
tech.root: Stg
ms.assetid: f1f0564e-0ecd-4b73-8863-9d6b6746fd02
ms.date: 12/05/2018
ms.keywords: IStorage interface [Structured Storage],OpenStorage method, IStorage.OpenStorage, IStorage::OpenStorage, OpenStorage, OpenStorage method [Structured Storage], OpenStorage method [Structured Storage],IStorage interface, _stg_istorage_openstorage, objidl/IStorage::OpenStorage, stg.istorage_openstorage
f1_keywords:
- objidl/IStorage.OpenStorage
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
- IStorage.OpenStorage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorage::OpenStorage


## -description


The <b>OpenStorage</b> method
			 opens an existing storage object with the specified name in the specified access mode.


## -parameters




### -param pwcsName [in]

A pointer to a wide character null-terminated Unicode string that contains the name of the storage object to open. The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE. This is a compound file restriction, not a structured storage restriction. It is ignored if <i>pstgPriority</i> is non-<b>NULL</b>.


### -param pstgPriority [in]

Must be <b>NULL</b>. A non-<b>NULL</b> value will return STG_E_INVALIDPARAMETER.


### -param grfMode [in]

Specifies the access mode to use when opening the storage object. For descriptions of the possible values, see <a href="https://docs.microsoft.com/windows/desktop/Stg/stgm-constants">STGM Constants</a>. Other modes you choose must at least specify STGM_SHARE_EXCLUSIVE when calling this method.


### -param snbExclude [in]

Must be <b>NULL</b>. A non-<b>NULL</b> value will return STG_E_INVALIDPARAMETER.


### -param reserved [in]

Reserved for future use; must be zero.


### -param ppstg [out]

When successful, pointer to the location of an 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to the opened storage object. This parameter is set to <b>NULL</b> if an error occurs.


## -returns



This method can return one of these values.




## -remarks



If the <i>pstgPriority</i> parameter is <b>NULL</b>, it is ignored. If the <i>pstgPriority</i> parameter is not <b>NULL</b>, it is an 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> pointer to a previous opening of an element of the storage object, usually one that was opened in priority mode. The storage object should be closed and reopened according to <i>grfMode</i>. When the <b>IStorage::OpenStorage</b> method returns, <i>pstgPriority</i> is no longer valid. Use the value supplied in the <i>ppstg</i> parameter.

Storage objects can be opened with STGM_DELETEONRELEASE, in which case the object is destroyed when it receives its final release. This is useful for creating temporary storage objects.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-createstorage">IStorage::CreateStorage</a>
 

 

