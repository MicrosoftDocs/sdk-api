---
UID: NF:wmdxva.IWMPlayerTimestampHook.MapTimestamp
title: IWMPlayerTimestampHook::MapTimestamp (wmdxva.h)
description: The MapTimestamp method is called by the WMV Decoder DMO to enable the source filter to provide the decoder with a time stamp. The decoder applies the time stamp to the sample before delivering the sample to the video renderer.
helpviewer_keywords: ["IWMPlayerTimestampHook interface [windows Media Format]","MapTimestamp method","IWMPlayerTimestampHook.MapTimestamp","IWMPlayerTimestampHook::MapTimestamp","IWMPlayerTimestampHookMapTimestamp","MapTimestamp","MapTimestamp method [windows Media Format]","MapTimestamp method [windows Media Format]","IWMPlayerTimestampHook interface","wmdxva/IWMPlayerTimestampHook::MapTimestamp","wmformat.iwmplayertimestamphook_maptimestamp"]
old-location: wmformat\iwmplayertimestamphook_maptimestamp.htm
tech.root: wmformat
ms.assetid: 67da583f-85da-4a09-be2c-44cf96bf51e7
ms.date: 4/26/2023
ms.keywords: IWMPlayerTimestampHook interface [windows Media Format],MapTimestamp method, IWMPlayerTimestampHook.MapTimestamp, IWMPlayerTimestampHook::MapTimestamp, IWMPlayerTimestampHookMapTimestamp, MapTimestamp, MapTimestamp method [windows Media Format], MapTimestamp method [windows Media Format],IWMPlayerTimestampHook interface, wmdxva/IWMPlayerTimestampHook::MapTimestamp, wmformat.iwmplayertimestamphook_maptimestamp
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPlayerTimestampHook::MapTimestamp
 - wmdxva/IWMPlayerTimestampHook::MapTimestamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmdxva.h
api_name:
 - IWMPlayerTimestampHook.MapTimestamp
---

# IWMPlayerTimestampHook::MapTimestamp


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MapTimestamp</b> method is called by the WMV Decoder DMO to enable the source filter to provide the decoder with a time stamp. The decoder applies the time stamp to the sample before delivering the sample to the video renderer.

## -parameters

### -param rtIn [in]

Time stamp previously applied by the DMO.

### -param prtOut [out]

Time stamp to be applied to the sample.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code .

## -see-also

<a href="/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>



<a href="/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook">IWMPlayerTimestampHook Interface</a>