---
UID: NF:amvideo.IQualProp.get_DevSyncOffset
title: IQualProp::get_DevSyncOffset (amvideo.h)
description: The get_DevSyncOffset method retrieves the average time difference between when the video frames should have been displayed and when they actually were.
helpviewer_keywords: ["IQualProp interface [DirectShow]","get_DevSyncOffset method","IQualProp.get_DevSyncOffset","IQualProp::get_DevSyncOffset","IQualPropget_DevSyncOffset","amvideo/IQualProp::get_DevSyncOffset","dshow.iqualprop_get_devsyncoffset","get_DevSyncOffset","get_DevSyncOffset method [DirectShow]","get_DevSyncOffset method [DirectShow]","IQualProp interface"]
old-location: dshow\iqualprop_get_devsyncoffset.htm
tech.root: dshow
ms.assetid: 69160479-7c72-46ed-9421-2a6c2c2861db
ms.date: 4/26/2023
ms.keywords: IQualProp interface [DirectShow],get_DevSyncOffset method, IQualProp.get_DevSyncOffset, IQualProp::get_DevSyncOffset, IQualPropget_DevSyncOffset, amvideo/IQualProp::get_DevSyncOffset, dshow.iqualprop_get_devsyncoffset, get_DevSyncOffset, get_DevSyncOffset method [DirectShow], get_DevSyncOffset method [DirectShow],IQualProp interface
req.header: amvideo.h
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
 - IQualProp::get_DevSyncOffset
 - amvideo/IQualProp::get_DevSyncOffset
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
 - IQualProp.get_DevSyncOffset
---

# IQualProp::get_DevSyncOffset


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_DevSyncOffset</code> method retrieves the average time difference between when the video frames should have been displayed and when they actually were. This method is the same as the <a href="/windows/desktop/api/amvideo/nf-amvideo-iqualprop-get_avgsyncoffset">IQualProp::get_AvgSyncOffset</a> method except that the value returned is calculated as a standard deviation rather than as a simple average.

## -parameters

### -param piDev

Pointer to a value denoting the accuracy of the video frames displayed.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

When playing video from networks, the presentation can often be disrupted by network glitches. For this reason, expressing the accuracy of video frames by a simple average is inappropriate. Looking at a standard deviation provides a better idea of the overall accuracy.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-iqualprop">IQualProp Interface</a>