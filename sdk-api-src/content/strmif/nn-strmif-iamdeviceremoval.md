---
UID: NN:strmif.IAMDeviceRemoval
title: IAMDeviceRemoval (strmif.h)
description: The IAMDeviceRemoval interface provides a way for the Filter Graph Manager to register for device removal events for a capture device.
helpviewer_keywords: ["IAMDeviceRemoval","IAMDeviceRemoval interface [DirectShow]","IAMDeviceRemoval interface [DirectShow]","described","IAMDeviceRemovalInterface","dshow.iamdeviceremoval","strmif/IAMDeviceRemoval"]
old-location: dshow\iamdeviceremoval.htm
tech.root: dshow
ms.assetid: 3d67f577-9d85-47ca-b887-f259e9acc964
ms.date: 4/26/2023
ms.keywords: IAMDeviceRemoval, IAMDeviceRemoval interface [DirectShow], IAMDeviceRemoval interface [DirectShow],described, IAMDeviceRemovalInterface, dshow.iamdeviceremoval, strmif/IAMDeviceRemoval
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMDeviceRemoval
 - strmif/IAMDeviceRemoval
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
 - IAMDeviceRemoval
---

# IAMDeviceRemoval interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMDeviceRemoval</code> interface provides a way for the Filter Graph Manager to register for device removal events for a capture device. The KsProxy filter exposes this interface. (See <a href="/windows/desktop/DirectShow/wdm-video-capture-filter">WDM Video Capture Filter</a>.)

Applications typically do not use this interface, and third-party filters do not need to implement this interface. To get a pointer to this interface, call <b>QueryInterface</b> on the KsProxy filter.

## -inheritance

The <b>IAMDeviceRemoval</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMDeviceRemoval</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
