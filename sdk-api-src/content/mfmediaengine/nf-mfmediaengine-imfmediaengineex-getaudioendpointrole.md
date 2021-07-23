---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetAudioEndpointRole
title: IMFMediaEngineEx::GetAudioEndpointRole (mfmediaengine.h)
description: Gets the audio device endpoint role used for the next call to SetSource or Load.
helpviewer_keywords: ["GetAudioEndpointRole","GetAudioEndpointRole method [Media Foundation]","GetAudioEndpointRole method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetAudioEndpointRole method","IMFMediaEngineEx.GetAudioEndpointRole","IMFMediaEngineEx::GetAudioEndpointRole","mf.imfmediaengineex_getaudioendpointrole","mfmediaengine/IMFMediaEngineEx::GetAudioEndpointRole"]
old-location: mf\imfmediaengineex_getaudioendpointrole.htm
tech.root: mf
ms.assetid: f63fa14e-44e6-41b9-a8c9-4b8eb66e98e0
ms.date: 12/05/2018
ms.keywords: GetAudioEndpointRole, GetAudioEndpointRole method [Media Foundation], GetAudioEndpointRole method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetAudioEndpointRole method, IMFMediaEngineEx.GetAudioEndpointRole, IMFMediaEngineEx::GetAudioEndpointRole, mf.imfmediaengineex_getaudioendpointrole, mfmediaengine/IMFMediaEngineEx::GetAudioEndpointRole
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
 - IMFMediaEngineEx::GetAudioEndpointRole
 - mfmediaengine/IMFMediaEngineEx::GetAudioEndpointRole
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
 - IMFMediaEngineEx.GetAudioEndpointRole
---

# IMFMediaEngineEx::GetAudioEndpointRole


## -description

Gets the audio device endpoint role used for the next  call to <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>.

## -parameters

### -param pRole [out]

Receives the audio endpoint role.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For information on audio endpoint roles, see <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole">ERole  enumeration</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>