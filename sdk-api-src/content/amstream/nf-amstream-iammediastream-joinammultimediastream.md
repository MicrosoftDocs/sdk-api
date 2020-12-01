---
UID: NF:amstream.IAMMediaStream.JoinAMMultiMediaStream
title: IAMMediaStream::JoinAMMultiMediaStream (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IAMMultiMediaStream::AddMediaStream method calls this method, which adds the specified media stream to the current multimedia stream.
helpviewer_keywords: ["IAMMediaStream interface [DirectShow]","JoinAMMultiMediaStream method","IAMMediaStream.JoinAMMultiMediaStream","IAMMediaStream::JoinAMMultiMediaStream","IAMMediaStreamJoinAMMultiMediaStream","JoinAMMultiMediaStream","JoinAMMultiMediaStream method [DirectShow]","JoinAMMultiMediaStream method [DirectShow]","IAMMediaStream interface","amstream/IAMMediaStream::JoinAMMultiMediaStream","dshow.iammediastream_joinammultimediastream"]
old-location: dshow\iammediastream_joinammultimediastream.htm
tech.root: dshow
ms.assetid: c842b841-a4dc-47c8-8186-347aff2c4ac3
ms.date: 12/05/2018
ms.keywords: IAMMediaStream interface [DirectShow],JoinAMMultiMediaStream method, IAMMediaStream.JoinAMMultiMediaStream, IAMMediaStream::JoinAMMultiMediaStream, IAMMediaStreamJoinAMMultiMediaStream, JoinAMMultiMediaStream, JoinAMMultiMediaStream method [DirectShow], JoinAMMultiMediaStream method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::JoinAMMultiMediaStream, dshow.iammediastream_joinammultimediastream
req.header: amstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaStream::JoinAMMultiMediaStream
 - amstream/IAMMediaStream::JoinAMMultiMediaStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaStream.JoinAMMultiMediaStream
---

# IAMMediaStream::JoinAMMultiMediaStream


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <a href="/windows/desktop/api/amstream/nf-amstream-iammultimediastream-addmediastream">IAMMultiMediaStream::AddMediaStream</a> method calls this method, which adds the specified media stream to the current multimedia stream.

## -parameters

### -param pAMMultiMediaStream [in]

Pointer to the <a href="/windows/desktop/api/amstream/nn-amstream-iammultimediastream">IAMMultiMediaStream</a> object to add the current media stream to.

## -returns

Returns S_OK if successful or MS_E_SAMPLEALLOC if the media stream already has allocated stream samples.

## -remarks

Don't increment the reference count of the supplied multimedia stream because it is already accounted for when created.

Applications should not call this method.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediastream">IAMMediaStream Interface</a>