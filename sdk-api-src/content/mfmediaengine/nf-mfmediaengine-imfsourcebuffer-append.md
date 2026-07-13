---
UID: NF:mfmediaengine.IMFSourceBuffer.Append
title: IMFSourceBuffer::Append (mfmediaengine.h)
description: Appends the specified media segment to the IMFSourceBuffer.
helpviewer_keywords: ["Append","Append method [Media Foundation]","Append method [Media Foundation]","IMFSourceBuffer interface","IMFSourceBuffer interface [Media Foundation]","Append method","IMFSourceBuffer.Append","IMFSourceBuffer::Append","mf.imfsourcebuffer_append","mfmediaengine/IMFSourceBuffer::Append"]
old-location: mf\imfsourcebuffer_append.htm
tech.root: mf
ms.assetid: 824fa23d-57d9-411a-af8a-fb65dca124b2
ms.date: 12/05/2018
ms.keywords: Append, Append method [Media Foundation], Append method [Media Foundation],IMFSourceBuffer interface, IMFSourceBuffer interface [Media Foundation],Append method, IMFSourceBuffer.Append, IMFSourceBuffer::Append, mf.imfsourcebuffer_append, mfmediaengine/IMFSourceBuffer::Append
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFSourceBuffer::Append
 - mfmediaengine/IMFSourceBuffer::Append
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFSourceBuffer.Append
---

# IMFSourceBuffer::Append


## -description

Appends the specified media segment to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a>.

## -parameters

### -param pData [in]

The media data to append.

### -param len [in]

The length of the media data stored in <i>pData</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a>