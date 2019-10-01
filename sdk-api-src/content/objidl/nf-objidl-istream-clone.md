---
UID: NF:objidl.IStream.Clone
title: IStream::Clone (objidl.h)
author: windows-sdk-content
description: The Clone method creates a new stream object with its own seek pointer that references the same bytes as the original stream.
old-location: stg\istream_clone.htm
tech.root: Stg
ms.assetid: 677c37fb-598f-4bb0-b5d6-600e0befc722
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IStream interface, IStream interface [Structured Storage],Clone method, IStream.Clone, IStream::Clone, _stg_istream_clone, objidl/IStream::Clone, stg.istream_clone
ms.topic: method
f1_keywords: 
 - "objidl/IStream.Clone"
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
 - IStream.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStream::Clone


## -description


The <b>Clone</b> method creates a new stream object with its own seek pointer that references the same bytes as the original stream.


## -parameters




### -param ppstm [out]

When successful, pointer to the location of an 
<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer to the new stream object. If an error occurs, this parameter is <b>NULL</b>.


## -returns



This method can return one of these values.




## -remarks



The <b>Clone</b> method creates a new stream object for accessing the same bytes but using a separate seek pointer. The new stream object sees the same data as the source-stream object. Changes written to one object are immediately visible in the other. Range locking is shared between the stream objects.

The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-copyto">IStream::CopyTo</a>
 

 

