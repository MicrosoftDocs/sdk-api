---
UID: NF:objidl.ILayoutStorage.ReLayoutDocfile
title: ILayoutStorage::ReLayoutDocfile (objidl.h)
description: The ReLayoutDocfile method rewrites the compound file, using the layout script obtained through monitoring, or provided through explicit layout scripting, to create a new compound file.
helpviewer_keywords: ["ILayoutStorage interface [Structured Storage]","ReLayoutDocfile method","ILayoutStorage.ReLayoutDocfile","ILayoutStorage::ReLayoutDocfile","ReLayoutDocfile","ReLayoutDocfile method [Structured Storage]","ReLayoutDocfile method [Structured Storage]","ILayoutStorage interface","_stg_ilayoutstorage_relayoutdocfile","objidl/ILayoutStorage::ReLayoutDocfile","stg.ilayoutstorage_relayoutdocfile"]
old-location: stg\ilayoutstorage_relayoutdocfile.htm
tech.root: Stg
ms.assetid: 5db3a26c-595a-4c9b-bb6d-b170eb9864df
ms.date: 12/05/2018
ms.keywords: ILayoutStorage interface [Structured Storage],ReLayoutDocfile method, ILayoutStorage.ReLayoutDocfile, ILayoutStorage::ReLayoutDocfile, ReLayoutDocfile, ReLayoutDocfile method [Structured Storage], ReLayoutDocfile method [Structured Storage],ILayoutStorage interface, _stg_ilayoutstorage_relayoutdocfile, objidl/ILayoutStorage::ReLayoutDocfile, stg.ilayoutstorage_relayoutdocfile
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
 - ILayoutStorage::ReLayoutDocfile
 - objidl/ILayoutStorage::ReLayoutDocfile
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
 - ILayoutStorage.ReLayoutDocfile
---

# ILayoutStorage::ReLayoutDocfile


## -description

The <b>ReLayoutDocfile</b> method rewrites the compound file, using the layout script obtained through monitoring, or provided through explicit layout scripting, to create a new compound file.

## -parameters

### -param pwcsNewDfName [in]

Pointer to the name of the compound file to be rewritten. This name must be a valid filename, distinct from the name of the original compound file. The original compound file will be optimized and written to the new <i>pwcsNewDfName</i>.

## -returns

This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as the following:

| Return code | Description |
|----------------|---------------|
|STG_E_INVALIDNAME | The name passed to this function is not a valid file name.|
|STG_E_UNKNOWN | The layout information has been corrupted and cannot be processed.|

