---
UID: NF:mfmediaengine.IMFMediaSourceExtension.RemoveSourceBuffer
title: IMFMediaSourceExtension::RemoveSourceBuffer (mfmediaengine.h)
description: Removes the specified source buffer from the collection of source buffers managed by the IMFMediaSourceExtension object.
helpviewer_keywords: ["IMFMediaSourceExtension interface [Media Foundation]","RemoveSourceBuffer method","IMFMediaSourceExtension.RemoveSourceBuffer","IMFMediaSourceExtension::RemoveSourceBuffer","RemoveSourceBuffer","RemoveSourceBuffer method [Media Foundation]","RemoveSourceBuffer method [Media Foundation]","IMFMediaSourceExtension interface","mf.imfmediasourceextension_removesourcebuffer","mfmediaengine/IMFMediaSourceExtension::RemoveSourceBuffer"]
old-location: mf\imfmediasourceextension_removesourcebuffer.htm
tech.root: mf
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
ms.date: 12/05/2018
ms.keywords: IMFMediaSourceExtension interface [Media Foundation],RemoveSourceBuffer method, IMFMediaSourceExtension.RemoveSourceBuffer, IMFMediaSourceExtension::RemoveSourceBuffer, RemoveSourceBuffer, RemoveSourceBuffer method [Media Foundation], RemoveSourceBuffer method [Media Foundation],IMFMediaSourceExtension interface, mf.imfmediasourceextension_removesourcebuffer, mfmediaengine/IMFMediaSourceExtension::RemoveSourceBuffer
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
 - IMFMediaSourceExtension::RemoveSourceBuffer
 - mfmediaengine/IMFMediaSourceExtension::RemoveSourceBuffer
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
 - IMFMediaSourceExtension.RemoveSourceBuffer
---

# IMFMediaSourceExtension::RemoveSourceBuffer


## -description

Removes the specified source buffer from the collection of source buffers managed by the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a> object.

## -parameters

### -param pSourceBuffer [in]

The buffer to remove.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>