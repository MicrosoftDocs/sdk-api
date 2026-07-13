---
UID: NF:objidl.IStream.Commit
title: IStream::Commit (objidl.h)
description: The Commit method ensures that any changes made to a stream object open in transacted mode are reflected in the parent storage.
helpviewer_keywords: ["Commit","Commit method [Structured Storage]","Commit method [Structured Storage]","IStream interface","IStream interface [Structured Storage]","Commit method","IStream.Commit","IStream::Commit","_stg_istream_commit","objidl/IStream::Commit","stg.istream_commit"]
old-location: stg\istream_commit.htm
tech.root: Stg
ms.assetid: 335c3a53-ca6a-42f3-bbf9-684ed48591e6
ms.date: 12/05/2018
ms.keywords: Commit, Commit method [Structured Storage], Commit method [Structured Storage],IStream interface, IStream interface [Structured Storage],Commit method, IStream.Commit, IStream::Commit, _stg_istream_commit, objidl/IStream::Commit, stg.istream_commit
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
 - IStream::Commit
 - objidl/IStream::Commit
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
 - IStream.Commit
---

# IStream::Commit


## -description

The <b>Commit</b>  method ensures that any changes made to a stream object open in transacted mode are reflected in the parent storage. If the stream object is open in direct mode, <b>IStream::Commit</b> has no effect other than flushing all memory buffers to the next-level storage object. The COM compound file implementation of streams does not support opening streams in transacted mode.

## -parameters

### -param grfCommitFlags [in]

Controls how the changes for the stream object are committed. See the 
<a href="/windows/desktop/api/wtypes/ne-wtypes-stgc">STGC</a> enumeration for a definition of these values.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | Changes to the stream object were successfully committed to the parent level.|
|E_PENDING | Asynchronous Storage only: Part or all of the stream's data is currently unavailable. |
|STG_E_MEDIUMFULL | The commit operation failed due to lack of space on the storage device.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

The <b>Commit</b>  method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage. Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object. If the parent is opened in transacted mode, the parent may revert at a later time, rolling back the changes to this stream object. The compound file implementation does not support the opening of streams in transacted mode, so this method has very little effect other than to flush memory buffers. For more information, see 
<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>.

If the stream is open in direct mode, this method ensures that any memory buffers have been flushed out to the underlying storage object. This is much like a flush in traditional file systems.

The <b>IStream::Commit</b> method is useful on a direct mode stream when the implementation of the 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface is a wrapper for underlying file system APIs. In this case, <b>IStream::Commit</b> would be connected to the file system's flush call.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>



<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>