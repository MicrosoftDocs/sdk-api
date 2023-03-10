---
UID: NF:objidl.ILayoutStorage.LayoutScript
title: ILayoutStorage::LayoutScript (objidl.h)
description: The LayoutScript method provides explicit directions for reordering the storages, streams, and controls in a compound file to match the order in which they are accessed during the download.
helpviewer_keywords: ["ILayoutStorage interface [Structured Storage]","LayoutScript method","ILayoutStorage.LayoutScript","ILayoutStorage::LayoutScript","LayoutScript","LayoutScript method [Structured Storage]","LayoutScript method [Structured Storage]","ILayoutStorage interface","_stg_ilayoutstorage_layoutscript","objidl/ILayoutStorage::LayoutScript","stg.ilayoutstorage_layoutscript"]
old-location: stg\ilayoutstorage_layoutscript.htm
tech.root: Stg
ms.assetid: 22ae3485-15d9-47e4-988e-fb760e67595b
ms.date: 12/05/2018
ms.keywords: ILayoutStorage interface [Structured Storage],LayoutScript method, ILayoutStorage.LayoutScript, ILayoutStorage::LayoutScript, LayoutScript, LayoutScript method [Structured Storage], LayoutScript method [Structured Storage],ILayoutStorage interface, _stg_ilayoutstorage_layoutscript, objidl/ILayoutStorage::LayoutScript, stg.ilayoutstorage_layoutscript
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
 - ILayoutStorage::LayoutScript
 - objidl/ILayoutStorage::LayoutScript
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
 - ILayoutStorage.LayoutScript
---

# ILayoutStorage::LayoutScript


## -description

The <b>LayoutScript</b> method provides explicit directions for reordering the storages, streams, and controls in a compound file to match the order in which they are accessed during the download.

## -parameters

### -param pStorageLayout [in]

Pointer to an array of 
<a href="/windows/desktop/api/objidl/ns-objidl-storagelayout">StorageLayout</a> structures.

### -param nEntries [in]

Number of entries in the array of 
<a href="/windows/desktop/api/objidl/ns-objidl-storagelayout">StorageLayout</a> structures.

### -param glfInterleavedFlag [in]

Reserved for future use.

## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as the following:

| Return code | Description |
|----------------|---------------|
|STG_E_INVALIDPOINTER | The storage layout pointer is invalid.|
|STG_E_INVALIDFLAG | The value of *glfInterleavedFlag* is invalid.|
|STG_E_PATHNOTFOUND | The new document file name specified is invalid.|
|STG_E_INSUFFICIENTMEMORY | There is not enough memory to complete the operation.|
|STG_E_INVALIDPARAMETER | One of the parameters is invalid.|
| STG_E_INUSE | The **BeginMonitor** method was called while **ILayoutStorage** was already monitoring.|

## -remarks

To provide explicit layout instructions, the application calls <b>ILayoutStorage::LayoutScript</b>, passing an array of 
<a href="/windows/desktop/api/objidl/ns-objidl-storagelayout">StorageLayout</a> structures. Each structure defines a single storage or stream data block and specifies where the block is to be written in the 
<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a> byte array.

An application can combine scripted layout with monitoring, as the structure of a particular compound file may dictate.

When the optimal data-layout pattern of an entire compound file has been determined, the application calls 
<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-relayoutdocfile">ILayoutStorage::ReLayoutDocfile</a> to restructure the compound file to match the order in which its data sectors were accessed.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-ilayoutstorage-relayoutdocfile">ILayoutStorage::ReLayoutDocfile</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ilockbytes">ILockBytes</a>



<a href="/windows/desktop/api/objidl/ns-objidl-storagelayout">StorageLayout</a>