---
UID: NF:mfidl.IMFVideoRendererEffectControl.OnAppServiceConnectionEstablished
tech.root: mf
title: IMFVideoRendererEffectControl::OnAppServiceConnectionEstablished
ms.date: 09/10/2025
targetos: Windows
description: Called asynchronously by the platform on successful establishment of a requested communication channel with a video renderer effect.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1803
req.target-min-winversvr: Windows Server version 1803
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFVideoRendererEffectControl::OnAppServiceConnectionEstablished
f1_keywords:
 - IMFVideoRendererEffectControl::OnAppServiceConnectionEstablished
 - mfidl/IMFVideoRendererEffectControl::OnAppServiceConnectionEstablished
dev_langs:
 - c++
helpviewer_keywords:
 - OnAppServiceConnectionEstablished
---

## -description

Called asynchronously by the platform on successful establishment of a requested communication channel with a video renderer effect.

## -parameters

### -param pAppServiceConnection

An **IUnknown** representing the app service connection object.

## -returns

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks


This method is called asynchronously after the video renderer effect sets the [MF_VIDEO_RENDERER_EFFECT_APP_SERVICE_NAME](/windows/win32/medfound/mf-video-renderer-effect-app-service-name) property.

## -see-also

