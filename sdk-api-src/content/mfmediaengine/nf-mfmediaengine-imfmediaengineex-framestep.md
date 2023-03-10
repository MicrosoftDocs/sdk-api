---
UID: NF:mfmediaengine.IMFMediaEngineEx.FrameStep
title: IMFMediaEngineEx::FrameStep (mfmediaengine.h)
description: Steps forward or backward one frame.
helpviewer_keywords: ["FrameStep","FrameStep method [Media Foundation]","FrameStep method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","FrameStep method","IMFMediaEngineEx.FrameStep","IMFMediaEngineEx::FrameStep","mf.imfmediaengineex_framestep","mfmediaengine/IMFMediaEngineEx::FrameStep"]
old-location: mf\imfmediaengineex_framestep.htm
tech.root: mf
ms.assetid: 090B5B6F-E4D1-43D7-AD09-BA3008B48104
ms.date: 12/05/2018
ms.keywords: FrameStep, FrameStep method [Media Foundation], FrameStep method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],FrameStep method, IMFMediaEngineEx.FrameStep, IMFMediaEngineEx::FrameStep, mf.imfmediaengineex_framestep, mfmediaengine/IMFMediaEngineEx::FrameStep
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
 - IMFMediaEngineEx::FrameStep
 - mfmediaengine/IMFMediaEngineEx::FrameStep
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
 - IMFMediaEngineEx.FrameStep
---

# IMFMediaEngineEx::FrameStep


## -description

Steps forward or backward one frame.

## -parameters

### -param Forward [in]

Specify <b>TRUE</b> to step forward or <b>FALSE</b> to step backward.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The frame-step direction is independent of the current playback direction.

This method completes asynchronously. When the operation completes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_FRAMESTEPCOMPLETED</b> event and enters the paused state.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>