---
UID: NF:mfmediaengine.IMFMediaSourceExtension.AddSourceBuffer
title: IMFMediaSourceExtension::AddSourceBuffer (mfmediaengine.h)
description: Adds a IMFSourceBuffer to the collection of buffers associated with the IMFMediaSourceExtension.
helpviewer_keywords: ["AddSourceBuffer","AddSourceBuffer method [Media Foundation]","AddSourceBuffer method [Media Foundation]","IMFMediaSourceExtension interface","IMFMediaSourceExtension interface [Media Foundation]","AddSourceBuffer method","IMFMediaSourceExtension.AddSourceBuffer","IMFMediaSourceExtension::AddSourceBuffer","mf.imfmediasourceextension_addsourcebuffer","mfmediaengine/IMFMediaSourceExtension::AddSourceBuffer"]
old-location: mf\imfmediasourceextension_addsourcebuffer.htm
tech.root: mf
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
ms.date: 12/05/2018
ms.keywords: AddSourceBuffer, AddSourceBuffer method [Media Foundation], AddSourceBuffer method [Media Foundation],IMFMediaSourceExtension interface, IMFMediaSourceExtension interface [Media Foundation],AddSourceBuffer method, IMFMediaSourceExtension.AddSourceBuffer, IMFMediaSourceExtension::AddSourceBuffer, mf.imfmediasourceextension_addsourcebuffer, mfmediaengine/IMFMediaSourceExtension::AddSourceBuffer
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
 - IMFMediaSourceExtension::AddSourceBuffer
 - mfmediaengine/IMFMediaSourceExtension::AddSourceBuffer
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
 - IMFMediaSourceExtension.AddSourceBuffer
---

# IMFMediaSourceExtension::AddSourceBuffer


## -description

Adds a <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> to the collection of buffers associated with the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>.

## -parameters

### -param type [in]

### -param pNotify [in]

### -param ppSourceBuffer [out]

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>