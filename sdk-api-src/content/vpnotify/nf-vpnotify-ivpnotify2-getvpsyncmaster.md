---
UID: NF:vpnotify.IVPNotify2.GetVPSyncMaster
title: IVPNotify2::GetVPSyncMaster (vpnotify.h)
description: The GetVPSyncMaster method checks whether the video port controls the synchronization of the VGA.
helpviewer_keywords: ["GetVPSyncMaster","GetVPSyncMaster method [DirectShow]","GetVPSyncMaster method [DirectShow]","IVPNotify2 interface","IVPNotify2 interface [DirectShow]","GetVPSyncMaster method","IVPNotify2.GetVPSyncMaster","IVPNotify2::GetVPSyncMaster","IVPNotify2GetVPSyncMaster","dshow.ivpnotify2_getvpsyncmaster","vpnotify/IVPNotify2::GetVPSyncMaster"]
old-location: dshow\ivpnotify2_getvpsyncmaster.htm
tech.root: dshow
ms.assetid: afc75615-1be5-4f1f-ace2-f3a17420b591
ms.date: 4/26/2023
ms.keywords: GetVPSyncMaster, GetVPSyncMaster method [DirectShow], GetVPSyncMaster method [DirectShow],IVPNotify2 interface, IVPNotify2 interface [DirectShow],GetVPSyncMaster method, IVPNotify2.GetVPSyncMaster, IVPNotify2::GetVPSyncMaster, IVPNotify2GetVPSyncMaster, dshow.ivpnotify2_getvpsyncmaster, vpnotify/IVPNotify2::GetVPSyncMaster
req.header: vpnotify.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPNotify2::GetVPSyncMaster
 - vpnotify/IVPNotify2::GetVPSyncMaster
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVPNotify2.GetVPSyncMaster
---

# IVPNotify2::GetVPSyncMaster


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetVPSyncMaster</code> method checks whether the video port controls the synchronization of the VGA.

## -parameters

### -param pbVPSyncMaster [out]

Pointer to a value indicating whether the video port controls the vertical synchronization of the VGA monitor. <b>TRUE</b> if the port controls the monitor's synchronization; <b>FALSE</b> otherwise.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Include Vptype.h before Vpnotify.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2">IVPNotify2 Interface</a>