---
UID: NF:strmif.IVMRMixerControl.GetMixingPrefs
title: IVMRMixerControl::GetMixingPrefs (strmif.h)
description: Retrieves the mixing preferences for the stream.
helpviewer_keywords: ["GetMixingPrefs","GetMixingPrefs method [DirectShow]","GetMixingPrefs method [DirectShow]","IVMRMixerControl interface","IVMRMixerControl interface [DirectShow]","GetMixingPrefs method","IVMRMixerControl.GetMixingPrefs","IVMRMixerControl::GetMixingPrefs","IVMRMixerControlGetMixingPrefs","dshow.ivmrmixercontrol_getmixingprefs","strmif/IVMRMixerControl::GetMixingPrefs"]
old-location: dshow\ivmrmixercontrol_getmixingprefs.htm
tech.root: dshow
ms.assetid: ee410a7e-e021-408a-bf40-cb58dc8eca1c
ms.date: 4/26/2023
ms.keywords: GetMixingPrefs, GetMixingPrefs method [DirectShow], GetMixingPrefs method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetMixingPrefs method, IVMRMixerControl.GetMixingPrefs, IVMRMixerControl::GetMixingPrefs, IVMRMixerControlGetMixingPrefs, dshow.ivmrmixercontrol_getmixingprefs, strmif/IVMRMixerControl::GetMixingPrefs
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRMixerControl::GetMixingPrefs
 - strmif/IVMRMixerControl::GetMixingPrefs
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
 - IVMRMixerControl.GetMixingPrefs
---

# IVMRMixerControl::GetMixingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Retrieves the mixing preferences for the stream.

## -parameters

### -param pdwMixerPrefs [in]

Address of a variable that receives a bitwise OR combination of <a href="/windows/desktop/api/strmif/ne-strmif-vmrmixerprefs">VMRMixerPrefs</a> flags.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>