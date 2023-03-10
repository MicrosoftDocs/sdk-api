---
UID: NF:mfmediaengine.IMFMediaSourceExtension.GetSourceBuffer
title: IMFMediaSourceExtension::GetSourceBuffer (mfmediaengine.h)
description: Gets the IMFSourceBuffer at the specified index in the collection of buffers.
helpviewer_keywords: ["GetSourceBuffer","GetSourceBuffer method [Media Foundation]","GetSourceBuffer method [Media Foundation]","IMFMediaSourceExtension interface","IMFMediaSourceExtension interface [Media Foundation]","GetSourceBuffer method","IMFMediaSourceExtension.GetSourceBuffer","IMFMediaSourceExtension::GetSourceBuffer","mf.imfmediasourceextension_getsourcebuffer","mfmediaengine/IMFMediaSourceExtension::GetSourceBuffer"]
old-location: mf\imfmediasourceextension_getsourcebuffer.htm
tech.root: mf
ms.assetid: ada32819-0ec3-4083-97a3-b8ae257d751b
ms.date: 12/05/2018
ms.keywords: GetSourceBuffer, GetSourceBuffer method [Media Foundation], GetSourceBuffer method [Media Foundation],IMFMediaSourceExtension interface, IMFMediaSourceExtension interface [Media Foundation],GetSourceBuffer method, IMFMediaSourceExtension.GetSourceBuffer, IMFMediaSourceExtension::GetSourceBuffer, mf.imfmediasourceextension_getsourcebuffer, mfmediaengine/IMFMediaSourceExtension::GetSourceBuffer
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
 - IMFMediaSourceExtension::GetSourceBuffer
 - mfmediaengine/IMFMediaSourceExtension::GetSourceBuffer
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
 - IMFMediaSourceExtension.GetSourceBuffer
---

# IMFMediaSourceExtension::GetSourceBuffer


## -description

Gets the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> at the specified index in the collection of buffers.

## -parameters

### -param dwStreamIndex [in]

The location of the buffer in the collection.

## -returns

The source buffer.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>