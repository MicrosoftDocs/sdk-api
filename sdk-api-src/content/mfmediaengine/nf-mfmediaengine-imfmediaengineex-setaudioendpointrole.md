---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetAudioEndpointRole
title: IMFMediaEngineEx::SetAudioEndpointRole (mfmediaengine.h)
author: windows-sdk-content
description: Sets the audio device endpoint used for the next call to SetSource or Load.
old-location: mf\imfmediaengineex_setaudioendpointrole.htm
tech.root: medfound
ms.assetid: 00fd78ce-e046-40a0-8bad-f4a1e1f517bb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetAudioEndpointRole method, IMFMediaEngineEx.SetAudioEndpointRole, IMFMediaEngineEx::SetAudioEndpointRole, SetAudioEndpointRole, SetAudioEndpointRole method [Media Foundation], SetAudioEndpointRole method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setaudioendpointrole, mfmediaengine/IMFMediaEngineEx::SetAudioEndpointRole
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineEx.SetAudioEndpointRole"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.SetAudioEndpointRole
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx::SetAudioEndpointRole


## -description


Sets the audio device endpoint used for the next call to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 


## -parameters




### -param role [in]

Specifies the audio end point role.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For information on audio endpoint roles, see <a href="https://docs.microsoft.com/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole">ERole  enumeration</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
 

 

