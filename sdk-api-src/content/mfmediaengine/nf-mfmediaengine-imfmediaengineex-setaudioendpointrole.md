---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetAudioEndpointRole
title: IMFMediaEngineEx::SetAudioEndpointRole (mfmediaengine.h)
description: Sets the audio device endpoint used for the next call to SetSource or Load.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetAudioEndpointRole method","IMFMediaEngineEx.SetAudioEndpointRole","IMFMediaEngineEx::SetAudioEndpointRole","SetAudioEndpointRole","SetAudioEndpointRole method [Media Foundation]","SetAudioEndpointRole method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_setaudioendpointrole","mfmediaengine/IMFMediaEngineEx::SetAudioEndpointRole"]
old-location: mf\imfmediaengineex_setaudioendpointrole.htm
tech.root: mf
ms.assetid: 00fd78ce-e046-40a0-8bad-f4a1e1f517bb
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetAudioEndpointRole method, IMFMediaEngineEx.SetAudioEndpointRole, IMFMediaEngineEx::SetAudioEndpointRole, SetAudioEndpointRole, SetAudioEndpointRole method [Media Foundation], SetAudioEndpointRole method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setaudioendpointrole, mfmediaengine/IMFMediaEngineEx::SetAudioEndpointRole
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
 - IMFMediaEngineEx::SetAudioEndpointRole
 - mfmediaengine/IMFMediaEngineEx::SetAudioEndpointRole
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
 - IMFMediaEngineEx.SetAudioEndpointRole
---

# IMFMediaEngineEx::SetAudioEndpointRole


## -description

Sets the audio device endpoint used for the next call to <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>.

## -parameters

### -param role [in]

Specifies the audio end point role.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For information on audio endpoint roles, see <a href="/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole">ERole  enumeration</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>