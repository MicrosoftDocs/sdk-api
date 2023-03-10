---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetRealTimeMode
title: IMFMediaEngineEx::SetRealTimeMode (mfmediaengine.h)
description: Sets the real time mode used for the next call to SetSource or Load.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetRealTimeMode method","IMFMediaEngineEx.SetRealTimeMode","IMFMediaEngineEx::SetRealTimeMode","SetRealTimeMode","SetRealTimeMode method [Media Foundation]","SetRealTimeMode method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_setrealtimemode","mfmediaengine/IMFMediaEngineEx::SetRealTimeMode"]
old-location: mf\imfmediaengineex_setrealtimemode.htm
tech.root: mf
ms.assetid: 31534f69-33ec-41d3-93aa-f4c457649e48
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetRealTimeMode method, IMFMediaEngineEx.SetRealTimeMode, IMFMediaEngineEx::SetRealTimeMode, SetRealTimeMode, SetRealTimeMode method [Media Foundation], SetRealTimeMode method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setrealtimemode, mfmediaengine/IMFMediaEngineEx::SetRealTimeMode
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
 - IMFMediaEngineEx::SetRealTimeMode
 - mfmediaengine/IMFMediaEngineEx::SetRealTimeMode
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
 - IMFMediaEngineEx.SetRealTimeMode
---

# IMFMediaEngineEx::SetRealTimeMode


## -description

Sets the real time mode used for the next call to  <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>.

## -parameters

### -param fEnable [in]

Specifies the real time mode.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>