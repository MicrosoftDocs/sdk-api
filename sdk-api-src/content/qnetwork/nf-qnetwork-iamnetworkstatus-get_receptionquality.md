---
UID: NF:qnetwork.IAMNetworkStatus.get_ReceptionQuality
title: IAMNetworkStatus::get_ReceptionQuality (qnetwork.h)
description: The get_ReceptionQuality method retrieves a value indicating the reception quality.
helpviewer_keywords: ["IAMNetworkStatus interface [DirectShow]","get_ReceptionQuality method","IAMNetworkStatus.get_ReceptionQuality","IAMNetworkStatus::get_ReceptionQuality","IAMNetworkStatusget_ReceptionQuality","dshow.iamnetworkstatus_get_receptionquality","get_ReceptionQuality","get_ReceptionQuality method [DirectShow]","get_ReceptionQuality method [DirectShow]","IAMNetworkStatus interface","qnetwork/IAMNetworkStatus::get_ReceptionQuality"]
old-location: dshow\iamnetworkstatus_get_receptionquality.htm
tech.root: dshow
ms.assetid: 6c80f874-c176-4e52-acc9-26c10fac08d9
ms.date: 4/26/2023
ms.keywords: IAMNetworkStatus interface [DirectShow],get_ReceptionQuality method, IAMNetworkStatus.get_ReceptionQuality, IAMNetworkStatus::get_ReceptionQuality, IAMNetworkStatusget_ReceptionQuality, dshow.iamnetworkstatus_get_receptionquality, get_ReceptionQuality, get_ReceptionQuality method [DirectShow], get_ReceptionQuality method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_ReceptionQuality
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMNetworkStatus::get_ReceptionQuality
 - qnetwork/IAMNetworkStatus::get_ReceptionQuality
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMNetworkStatus.get_ReceptionQuality
---

# IAMNetworkStatus::get_ReceptionQuality


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ReceptionQuality</code> method retrieves a value indicating the reception quality.

## -parameters

### -param pReceptionQuality

Pointer to a variable that receives a value from 0 to 100, indicating the reception quality. This value is percentage of packets that the filter received without requiring resending or error correction.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamnetworkstatus">IAMNetworkStatus Interface</a>