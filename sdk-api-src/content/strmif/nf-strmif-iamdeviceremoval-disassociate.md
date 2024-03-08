---
UID: NF:strmif.IAMDeviceRemoval.Disassociate
title: IAMDeviceRemoval::Disassociate (strmif.h)
description: The Disassociate method disassociates the KsProxy filter from the device by closing the device handle. The Filter Graph Manager calls this method if it receives a notification that the device was removed.
helpviewer_keywords: ["Disassociate","Disassociate method [DirectShow]","Disassociate method [DirectShow]","IAMDeviceRemoval interface","IAMDeviceRemoval interface [DirectShow]","Disassociate method","IAMDeviceRemoval.Disassociate","IAMDeviceRemoval::Disassociate","IAMDeviceRemovalDisassociate","dshow.iamdeviceremoval_disassociate","strmif/IAMDeviceRemoval::Disassociate"]
old-location: dshow\iamdeviceremoval_disassociate.htm
tech.root: dshow
ms.assetid: cf868f5d-3ec1-4c01-9154-27420d136fe5
ms.date: 4/26/2023
ms.keywords: Disassociate, Disassociate method [DirectShow], Disassociate method [DirectShow],IAMDeviceRemoval interface, IAMDeviceRemoval interface [DirectShow],Disassociate method, IAMDeviceRemoval.Disassociate, IAMDeviceRemoval::Disassociate, IAMDeviceRemovalDisassociate, dshow.iamdeviceremoval_disassociate, strmif/IAMDeviceRemoval::Disassociate
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
 - IAMDeviceRemoval::Disassociate
 - strmif/IAMDeviceRemoval::Disassociate
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
 - IAMDeviceRemoval.Disassociate
---

# IAMDeviceRemoval::Disassociate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Disassociate</code> method disassociates the KsProxy filter from the device by closing the device handle. The Filter Graph Manager calls this method if it receives a notification that the device was removed.



## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdeviceremoval">IAMDeviceRemoval Interface</a>
