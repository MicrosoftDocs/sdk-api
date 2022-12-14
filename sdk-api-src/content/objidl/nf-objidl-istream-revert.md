---
UID: NF:objidl.IStream.Revert
title: IStream::Revert (objidl.h)
description: The Revert method discards all changes that have been made to a transacted stream since the last IStream::Commit call. On streams open in direct mode and streams using the COM compound file implementation of IStream::Revert, this method has no effect.
helpviewer_keywords: ["IStream interface [Structured Storage]","Revert method","IStream.Revert","IStream::Revert","Revert","Revert method [Structured Storage]","Revert method [Structured Storage]","IStream interface","_stg_istream_revert","objidl/IStream::Revert","stg.istream_revert"]
old-location: stg\istream_revert.htm
tech.root: Stg
ms.assetid: 1a707b17-840f-4cd2-9e43-97a8c02120b8
ms.date: 12/05/2018
ms.keywords: IStream interface [Structured Storage],Revert method, IStream.Revert, IStream::Revert, Revert, Revert method [Structured Storage], Revert method [Structured Storage],IStream interface, _stg_istream_revert, objidl/IStream::Revert, stg.istream_revert
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
 - IStream::Revert
 - objidl/IStream::Revert
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
 - IStream.Revert
---

# IStream::Revert


## -description

The <b>Revert</b> method discards all changes that have been made to a transacted stream since the last 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-commit">IStream::Commit</a> call. On streams open in direct mode and streams using the COM compound file implementation of <b>IStream::Revert</b>, this method has no effect.



## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The stream was successfully reverted to its previous version.|
|E_PENDING | Asynchronous Storage only: Part or all of the stream's data is currently unavailable. |

## -remarks

The <b>Revert</b> method discards changes made to a transacted stream since the last commit operation.

## -see-also

<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istream-commit">IStream::Commit</a>
