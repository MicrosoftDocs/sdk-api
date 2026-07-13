---
UID: NF:mfmediaengine.IMFMediaEngine.GetSeekable
title: IMFMediaEngine::GetSeekable (mfmediaengine.h)
description: Gets the time ranges to which the Media Engine can currently seek.
helpviewer_keywords: ["GetSeekable","GetSeekable method [Media Foundation]","GetSeekable method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetSeekable method","IMFMediaEngine.GetSeekable","IMFMediaEngine::GetSeekable","mf.imfmediaengine_getseekable","mfmediaengine/IMFMediaEngine::GetSeekable"]
old-location: mf\imfmediaengine_getseekable.htm
tech.root: mf
ms.assetid: FB238892-B172-4E31-B4E5-68C96E135345
ms.date: 12/05/2018
ms.keywords: GetSeekable, GetSeekable method [Media Foundation], GetSeekable method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetSeekable method, IMFMediaEngine.GetSeekable, IMFMediaEngine::GetSeekable, mf.imfmediaengine_getseekable, mfmediaengine/IMFMediaEngine::GetSeekable
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngine::GetSeekable
 - mfmediaengine/IMFMediaEngine::GetSeekable
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
 - IMFMediaEngine.GetSeekable
---

# IMFMediaEngine::GetSeekable


## -description

Gets the time ranges to which the Media Engine can currently seek.

## -parameters

### -param ppSeekable [out]

Receives a pointer to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange">IMFMediaTimeRange</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>seekable</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

To find out whether the media source supports seeking, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getresourcecharacteristics">IMFMediaEngineEx::GetResourceCharacteristics</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>