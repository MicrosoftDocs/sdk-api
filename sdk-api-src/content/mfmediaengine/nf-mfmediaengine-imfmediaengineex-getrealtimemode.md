---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetRealTimeMode
title: IMFMediaEngineEx::GetRealTimeMode (mfmediaengine.h)
description: Gets the real time mode used for the next call to SetSource or Load.
helpviewer_keywords: ["GetRealTimeMode","GetRealTimeMode method [Media Foundation]","GetRealTimeMode method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetRealTimeMode method","IMFMediaEngineEx.GetRealTimeMode","IMFMediaEngineEx::GetRealTimeMode","mf.imfmediaengineex_getrealtimemode","mfmediaengine/IMFMediaEngineEx::GetRealTimeMode"]
old-location: mf\imfmediaengineex_getrealtimemode.htm
tech.root: mf
ms.assetid: 473a2b5a-5b9d-4754-bd32-89c9c4ab8c4a
ms.date: 12/05/2018
ms.keywords: GetRealTimeMode, GetRealTimeMode method [Media Foundation], GetRealTimeMode method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetRealTimeMode method, IMFMediaEngineEx.GetRealTimeMode, IMFMediaEngineEx::GetRealTimeMode, mf.imfmediaengineex_getrealtimemode, mfmediaengine/IMFMediaEngineEx::GetRealTimeMode
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
 - IMFMediaEngineEx::GetRealTimeMode
 - mfmediaengine/IMFMediaEngineEx::GetRealTimeMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfmediaengine.h
api_name:
 - IMFMediaEngineEx.GetRealTimeMode
---

# IMFMediaEngineEx::GetRealTimeMode


## -description

Gets the real time mode used for the next call to <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>.

## -parameters

### -param pfEnabled [out]

Receives the real time mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>