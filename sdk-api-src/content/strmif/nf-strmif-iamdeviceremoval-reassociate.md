---
UID: NF:strmif.IAMDeviceRemoval.Reassociate
title: IAMDeviceRemoval::Reassociate (strmif.h)
description: The Reassociate method reassociates the KsProxy filter with the device. The Filter Graph Manager calls this method if it receives a notification that the device has returned after being removed.
helpviewer_keywords: ["IAMDeviceRemoval interface [DirectShow]","Reassociate method","IAMDeviceRemoval.Reassociate","IAMDeviceRemoval::Reassociate","IAMDeviceRemovalReassociate","Reassociate","Reassociate method [DirectShow]","Reassociate method [DirectShow]","IAMDeviceRemoval interface","dshow.iamdeviceremoval_reassociate","strmif/IAMDeviceRemoval::Reassociate"]
old-location: dshow\iamdeviceremoval_reassociate.htm
tech.root: dshow
ms.assetid: 214b98c7-4143-4466-a359-1e9c9e4c778d
ms.date: 4/26/2023
ms.keywords: IAMDeviceRemoval interface [DirectShow],Reassociate method, IAMDeviceRemoval.Reassociate, IAMDeviceRemoval::Reassociate, IAMDeviceRemovalReassociate, Reassociate, Reassociate method [DirectShow], Reassociate method [DirectShow],IAMDeviceRemoval interface, dshow.iamdeviceremoval_reassociate, strmif/IAMDeviceRemoval::Reassociate
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
 - IAMDeviceRemoval::Reassociate
 - strmif/IAMDeviceRemoval::Reassociate
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
 - IAMDeviceRemoval.Reassociate
---

# IAMDeviceRemoval::Reassociate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Reassociate</code> method reassociates the KsProxy filter with the device. The Filter Graph Manager calls this method if it receives a notification that the device has returned after being removed.



## -returns

If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdeviceremoval">IAMDeviceRemoval Interface</a>
