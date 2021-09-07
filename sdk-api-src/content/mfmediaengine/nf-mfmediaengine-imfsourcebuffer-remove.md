---
UID: NF:mfmediaengine.IMFSourceBuffer.Remove
title: IMFSourceBuffer::Remove (mfmediaengine.h)
description: Removes the media segments defined by the specified time range from the IMFSourceBuffer.
helpviewer_keywords: ["IMFSourceBuffer interface [Media Foundation]","Remove method","IMFSourceBuffer.Remove","IMFSourceBuffer::Remove","Remove","Remove method [Media Foundation]","Remove method [Media Foundation]","IMFSourceBuffer interface","mf.imfsourcebuffer_remove","mfmediaengine/IMFSourceBuffer::Remove"]
old-location: mf\imfsourcebuffer_remove.htm
tech.root: mf
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
ms.date: 12/05/2018
ms.keywords: IMFSourceBuffer interface [Media Foundation],Remove method, IMFSourceBuffer.Remove, IMFSourceBuffer::Remove, Remove, Remove method [Media Foundation], Remove method [Media Foundation],IMFSourceBuffer interface, mf.imfsourcebuffer_remove, mfmediaengine/IMFSourceBuffer::Remove
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
 - IMFSourceBuffer::Remove
 - mfmediaengine/IMFSourceBuffer::Remove
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
 - IMFSourceBuffer.Remove
---

# IMFSourceBuffer::Remove


## -description

Removes the media segments defined by the specified time range from the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a>.

## -parameters

### -param start [in]

The start of the time range.

### -param end [in]

The end of the time range.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a>