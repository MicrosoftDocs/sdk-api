---
UID: NF:wmdxva.IWMCodecAMVideoAccelerator.SetPlayerNotify
title: IWMCodecAMVideoAccelerator::SetPlayerNotify (wmdxva.h)
description: The SetPlayerNotify method is called by the output pin on the source filter to provide the decoder DMO with the source filter's IWMPlayerTimestampHook interface to enable the source filter to update the time stamps on the samples before they are delivered to the renderer.
helpviewer_keywords: ["IWMCodecAMVideoAccelerator interface [windows Media Format]","SetPlayerNotify method","IWMCodecAMVideoAccelerator.SetPlayerNotify","IWMCodecAMVideoAccelerator::SetPlayerNotify","IWMCodecAMVideoAcceleratorSetPlayerNotify","SetPlayerNotify","SetPlayerNotify method [windows Media Format]","SetPlayerNotify method [windows Media Format]","IWMCodecAMVideoAccelerator interface","wmdxva/IWMCodecAMVideoAccelerator::SetPlayerNotify","wmformat.iwmcodecamvideoaccelerator_setplayernotify"]
old-location: wmformat\iwmcodecamvideoaccelerator_setplayernotify.htm
tech.root: wmformat
ms.assetid: 3be015c4-a641-44b9-9be8-a76b5dd4f998
ms.date: 4/26/2023
ms.keywords: IWMCodecAMVideoAccelerator interface [windows Media Format],SetPlayerNotify method, IWMCodecAMVideoAccelerator.SetPlayerNotify, IWMCodecAMVideoAccelerator::SetPlayerNotify, IWMCodecAMVideoAcceleratorSetPlayerNotify, SetPlayerNotify, SetPlayerNotify method [windows Media Format], SetPlayerNotify method [windows Media Format],IWMCodecAMVideoAccelerator interface, wmdxva/IWMCodecAMVideoAccelerator::SetPlayerNotify, wmformat.iwmcodecamvideoaccelerator_setplayernotify
req.header: wmdxva.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMCodecAMVideoAccelerator::SetPlayerNotify
 - wmdxva/IWMCodecAMVideoAccelerator::SetPlayerNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMCodecAMVideoAccelerator.SetPlayerNotify
---

# IWMCodecAMVideoAccelerator::SetPlayerNotify


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetPlayerNotify</b> method is called by the output pin on the source filter to provide the decoder <a href="/windows/desktop/wmformat/wmformat-glossary">DMO</a> with the source filter's <b>IWMPlayerTimestampHook</b> interface to enable the source filter to update the time stamps on the samples before they are delivered to the renderer.

## -parameters

### -param pHook [in]

Pointer to the <b>IWMPlayerTimestampHook</b> interface exposed on the player.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator">IWMCodecAMVideoAccelerator Interface</a>