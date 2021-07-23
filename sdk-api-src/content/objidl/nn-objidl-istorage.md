---
UID: NN:objidl.IStorage
title: IStorage (objidl.h)
description: The IStorage interface supports the creation and management of structured storage objects.
helpviewer_keywords: ["IStorage","IStorage interface [Structured Storage]","IStorage interface [Structured Storage]","described","_stg_istorage","objidl/IStorage","stg.istorage"]
old-location: stg\istorage.htm
tech.root: Stg
ms.assetid: 2f454538-0f40-4811-b908-cd317ef79487
ms.date: 12/05/2018
ms.keywords: IStorage, IStorage interface [Structured Storage], IStorage interface [Structured Storage],described, _stg_istorage, objidl/IStorage, stg.istorage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorage
 - objidl/IStorage
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
 - IStorage
---

# IStorage interface


## -description

The 
<b>IStorage</b> interface supports the creation and management of structured storage objects. Structured storage allows hierarchical storage of information within a single file, and is often referred to as "a file system within a file". Elements of a structured storage object are storages and streams. Storages are analogous to directories, and streams are analogous to files. Within a structured storage there will be a primary storage object that may contain substorages, possibly nested, and streams. Storages provide the structure of the object, and streams contain the data, which is manipulated through the 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface.

The 
<b>IStorage</b> interface provides methods for creating and managing the root storage object, child storage objects, and stream objects. These methods can create, open, enumerate, move, copy, rename, or delete the elements in the storage object.

An application must release its 
<b>IStorage</b> pointers when it is done with the storage object to deallocate memory used. There are also methods for changing the date and time of an element.

There are a number of different modes in which a storage object and its elements can be opened, determined by setting values from <a href="/windows/desktop/Stg/stgm-constants">STGM Constants</a>. One aspect of this is how changes are committed. You can set direct mode, in which changes to an object are immediately written to it, or transacted mode, in which changes are written to a buffer until explicitly committed. The 
<b>IStorage</b> interface provides methods for committing changes and reverting to the last-committed version. For example, a stream can be opened in read-only mode or read/write mode. For more information, see <b>STGM Constants</b>.

Other methods provide access to information about a storage object and its elements through the 
<a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure.

## -inheritance

The <b>IStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStorage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="/windows/desktop/Stg/samples">Samples</a>
