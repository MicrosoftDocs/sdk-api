---
UID: NF:amvideo.IQualProp.get_AvgSyncOffset
title: IQualProp::get_AvgSyncOffset (amvideo.h)
description: The get_AvgSyncOffset method retrieves the average time difference between when the video frames should have been displayed and when they actually were.
helpviewer_keywords: ["IQualProp interface [DirectShow]","get_AvgSyncOffset method","IQualProp.get_AvgSyncOffset","IQualProp::get_AvgSyncOffset","IQualPropget_AvgSyncOffset","amvideo/IQualProp::get_AvgSyncOffset","dshow.iqualprop_get_avgsyncoffset","get_AvgSyncOffset","get_AvgSyncOffset method [DirectShow]","get_AvgSyncOffset method [DirectShow]","IQualProp interface"]
old-location: dshow\iqualprop_get_avgsyncoffset.htm
tech.root: dshow
ms.assetid: 4bed68f0-d080-46d4-b582-e561ddca33f0
ms.date: 4/26/2023
ms.keywords: IQualProp interface [DirectShow],get_AvgSyncOffset method, IQualProp.get_AvgSyncOffset, IQualProp::get_AvgSyncOffset, IQualPropget_AvgSyncOffset, amvideo/IQualProp::get_AvgSyncOffset, dshow.iqualprop_get_avgsyncoffset, get_AvgSyncOffset, get_AvgSyncOffset method [DirectShow], get_AvgSyncOffset method [DirectShow],IQualProp interface
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
 - IQualProp::get_AvgSyncOffset
 - amvideo/IQualProp::get_AvgSyncOffset
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
 - IQualProp.get_AvgSyncOffset
---

# IQualProp::get_AvgSyncOffset


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_AvgSyncOffset</code> method retrieves the average time difference between when the video frames should have been displayed and when they actually were.

## -parameters

### -param piAvg

Pointer to the time difference, expressed in milliseconds.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-iqualprop">IQualProp Interface</a>