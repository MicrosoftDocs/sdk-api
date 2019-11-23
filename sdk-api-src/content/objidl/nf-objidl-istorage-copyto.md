---
UID: NF:objidl.IStorage.CopyTo
title: IStorage::CopyTo (objidl.h)

description: Copies the entire contents of an open storage object to another storage object.
old-location: stg\istorage_copyto.htm
tech.root: Stg
ms.assetid: 8b25b32b-f739-406a-96e8-dba687c7f055

ms.date: 12/05/2018
ms.keywords: CopyTo, CopyTo method [Structured Storage], CopyTo method [Structured Storage],IStorage interface, IStorage interface [Structured Storage],CopyTo method, IStorage.CopyTo, IStorage::CopyTo, _stg_istorage_copyto, objidl/IStorage::CopyTo, stg.istorage_copyto
ms.topic: method
f1_keywords: 
 - "objidl/IStorage.CopyTo"
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
 - IStorage.CopyTo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorage::CopyTo


## -description


The <b>CopyTo</b> method copies the entire contents of an open storage object to another storage object.


## -parameters




### -param ciidExclude [in]

The number of elements in the array pointed to by <i>rgiidExclude</i>. If <i>rgiidExclude</i> is <b>NULL</b>, then <i>ciidExclude</i> is ignored.


### -param rgiidExclude [in]

An array of interface identifiers (IIDs) that either the caller knows about and does not want copied or that the storage object does not support, but whose state the caller will later explicitly copy. The array can include 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>, indicating that only stream objects are to be copied, and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>, indicating that only storage objects are to be copied. An array length of zero indicates that only the state exposed by the 
<b>IStorage</b> object is to be copied; all other interfaces on the object are to be ignored. Passing <b>NULL</b> indicates that all interfaces on the object are to be copied.


### -param snbExclude [in]

A string name block (refer to 
<a href="https://docs.microsoft.com/windows/desktop/Stg/snb">SNB</a>) that specifies a block of storage or stream objects that are not to be copied to the destination. These elements are not created at the destination. If <b>IID_IStorage</b> is in the <i>rgiidExclude</i> array, this parameter is ignored. This parameter may be <b>NULL</b>.


### -param pstgDest [in]

A pointer to the open storage object into which this storage object is to be copied. The destination storage object can be a different implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> interface from the source storage object. Thus, <b>IStorage::CopyTo</b> can use only publicly available methods of the destination storage object. If <i>pstgDest</i> is open in transacted mode, it can be reverted by calling its 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-revert">IStorage::Revert</a> method.


## -returns



This method can return one of these values.




## -remarks



This method merges elements contained in the source storage object with those already present in the destination. The layout of the destination storage object may differ from the source storage object.

The copy process is recursive, invoking <b>IStorage::CopyTo</b> and 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-copyto">IStream::CopyTo</a> on the elements nested inside the source.

When copying a stream on top of an existing stream with the same name, the existing stream is first removed and then replaced with the source stream. When copying a storage on top of an existing storage with the same name, the existing storage is not removed. As a result, after the copy operation, the destination 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a> contains older elements, unless they were replaced by newer ones with the same names.

A storage object may expose interfaces other than 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>, including 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irootstorage">IRootStorage</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>. The <i>rgiidExclude</i> parameter permits the exclusion of any or all of these additional interfaces from the copy operation.

A caller with a newer or more efficient copy of an existing substorage or stream object may want to exclude the current versions of these objects from the copy operation. The <i>snbExclude</i> and <i>rgiidExclude</i> parameters provide two ways of excluding a storage objects existing storages or streams.

<h3><a id="Note_to_Callers"></a><a id="note_to_callers"></a><a id="NOTE_TO_CALLERS"></a>Note to Callers</h3>
The most common way to use the <b>IStorage::CopyTo</b> method is to copy everything from the source to the destination, as in most full-save and save-as operations.

The following  example code shows how to copy everything  from the source storage object to the destination storage object.


```cpp
pstg->CopyTo(0, Null, Null, pstgDest)
```


<div class="alert"><b>Note</b>  To compact a document file, call <b>CopyTo</b> on the root storage object and copy to a new storage object.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istorage-compound-file-implementation">IStorage - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-moveelementto">IStorage::MoveElementTo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-revert">IStorage::Revert</a>
 

 

