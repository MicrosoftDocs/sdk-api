---
UID: NF:audioclient.IAudioClient2.SetClientProperties
title: IAudioClient2::SetClientProperties (audioclient.h)
description: Sets the properties of the audio stream by populating an AudioClientProperties structure.
helpviewer_keywords: ["IAudioClient2 interface [Core Audio]","SetClientProperties method","IAudioClient2.SetClientProperties","IAudioClient2::SetClientProperties","SetClientProperties","SetClientProperties method [Core Audio]","SetClientProperties method [Core Audio]","IAudioClient2 interface","audioclient/IAudioClient2::SetClientProperties","coreaudio.iaudioclient2_setclientproperties"]
old-location: coreaudio\iaudioclient2_setclientproperties.htm
tech.root: CoreAudio
ms.assetid: B9B98EF9-C0E1-430A-9C79-1B414F4D67B5
ms.date: 12/05/2018
ms.keywords: IAudioClient2 interface [Core Audio],SetClientProperties method, IAudioClient2.SetClientProperties, IAudioClient2::SetClientProperties, SetClientProperties, SetClientProperties method [Core Audio], SetClientProperties method [Core Audio],IAudioClient2 interface, audioclient/IAudioClient2::SetClientProperties, coreaudio.iaudioclient2_setclientproperties
req.header: audioclient.h
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
 - IAudioClient2::SetClientProperties
 - audioclient/IAudioClient2::SetClientProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient2.SetClientProperties
---

# IAudioClient2::SetClientProperties


## -description

Sets the properties of the audio stream by populating an <a href="/windows/win32/api/audioclient/ns-audioclient-audioclientproperties-r1">AudioClientProperties</a> structure.

## -parameters

### -param pProperties [in]

Pointer to an <a href="/windows/win32/api/audioclient/ns-audioclient-audioclientproperties-r1">AudioClientProperties</a> structure.

## -returns

The <b>SetClientProperties</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -remarks

Starting with Windows 10, hardware-offloaded audio streams must be event driven. This means that if you call <b>IAudioClient2::SetClientProperties</b> and set the <i>bIsOffload</i> parameter of the <a href="/windows/win32/api/audioclient/ns-audioclient-audioclientproperties~r1">AudioClientProperties</a> to TRUE, you must specify the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag in the <i>StreamFlags</i> parameter to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>.

## -see-also

<a href="/windows/win32/api/audioclient/ns-audioclient-audioclientproperties-r1">AudioClientProperties</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient2">IAudioClient2</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>