---
UID: NF:objidl.IStream.Commit
title: IStream::Commit
author: windows-sdk-content
description: The Commit method ensures that any changes made to a stream object open in transacted mode are reflected in the parent storage.
old-location: stg\istream_commit.htm
old-project: Stg
ms.assetid: 335c3a53-ca6a-42f3-bbf9-684ed48591e6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Commit, Commit method [Structured Storage], Commit method [Structured Storage],IStream interface, IStream interface [Structured Storage],Commit method, IStream.Commit, IStream::Commit, _stg_istream_commit, objidl/IStream::Commit, stg.istream_commit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IStream.Commit
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IStream::Commit


## -description


The <b>Commit</b>  method ensures that any changes made to a stream object open in transacted mode are reflected in the parent storage. If the stream object is open in direct mode, <b>IStream::Commit</b> has no effect other than flushing all memory buffers to the next-level storage object. The COM compound file implementation of streams does not support opening streams in transacted mode.


## -parameters




### -param grfCommitFlags [in]

Controls how the changes for the stream object are committed. See the 
<a href="https://msdn.microsoft.com/f37260c0-d03d-4ead-a342-d2454ce8b1ac">STGC</a> enumeration for a definition of these values.


## -returns



This method can return one of these values.




## -remarks



The <b>Commit</b>  method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage. Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object. If the parent is opened in transacted mode, the parent may revert at a later time, rolling back the changes to this stream object. The compound file implementation does not support the opening of streams in transacted mode, so this method has very little effect other than to flush memory buffers. For more information, see 
<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>.

If the stream is open in direct mode, this method ensures that any memory buffers have been flushed out to the underlying storage object. This is much like a flush in traditional file systems.

The <b>IStream::Commit</b> method is useful on a direct mode stream when the implementation of the 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface is a wrapper for underlying file system APIs. In this case, <b>IStream::Commit</b> would be connected to the file system's flush call.




## -see-also




<a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>



<a href="https://msdn.microsoft.com/52474e37-0e14-4dcc-8e04-4442cfd26eb3">IStream - Compound File Implementation</a>
 

 

