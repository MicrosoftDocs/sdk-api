---
UID: NF:strmif.IVPManager.GetVideoPortIndex
title: IVPManager::GetVideoPortIndex (strmif.h)
description: The GetVideoPortIndex method returns the current video port index being used by the Video Port Manager (VPM).
helpviewer_keywords: ["GetVideoPortIndex","GetVideoPortIndex method [DirectShow]","GetVideoPortIndex method [DirectShow]","IVPManager interface","IVPManager interface [DirectShow]","GetVideoPortIndex method","IVPManager.GetVideoPortIndex","IVPManager::GetVideoPortIndex","IVPManagerGetVideoPortIndex","dshow.ivpmanager_getvideoportindex","strmif/IVPManager::GetVideoPortIndex"]
old-location: dshow\ivpmanager_getvideoportindex.htm
tech.root: DirectShow
ms.assetid: 1e30c2d7-b986-47f5-94c8-53937d1e1501
ms.date: 4/26/2023
ms.keywords: GetVideoPortIndex, GetVideoPortIndex method [DirectShow], GetVideoPortIndex method [DirectShow],IVPManager interface, IVPManager interface [DirectShow],GetVideoPortIndex method, IVPManager.GetVideoPortIndex, IVPManager::GetVideoPortIndex, IVPManagerGetVideoPortIndex, dshow.ivpmanager_getvideoportindex, strmif/IVPManager::GetVideoPortIndex
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPManager::GetVideoPortIndex
 - strmif/IVPManager::GetVideoPortIndex
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
 - IVPManager.GetVideoPortIndex
---

# IVPManager::GetVideoPortIndex


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetVideoPortIndex</code> method returns the current video port index being used by the Video Port Manager (VPM).

## -parameters

### -param pdwVideoPortIndex [out]

Pointer to a double word containing the index of the video port that the VPM is currently connected to.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method returns the current video port index being used by the Video Port Manager (VPM).

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivpmanager">IVPManager Interface</a>



[SetVideoPortIndex](/windows/desktop/api/strmif/nf-strmif-ivpmanager-setvideoportindex)