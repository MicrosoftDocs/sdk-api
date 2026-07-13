---
UID: NF:wmsdkidl.IWMVideoMediaProps.SetMaxKeyFrameSpacing
title: IWMVideoMediaProps::SetMaxKeyFrameSpacing (wmsdkidl.h)
description: The SetMaxKeyFrameSpacing method specifies the maximum interval between key frames.
helpviewer_keywords: ["IWMVideoMediaProps interface [windows Media Format]","SetMaxKeyFrameSpacing method","IWMVideoMediaProps.SetMaxKeyFrameSpacing","IWMVideoMediaProps::SetMaxKeyFrameSpacing","IWMVideoMediaPropsSetMaxKeyFrameSpacing","SetMaxKeyFrameSpacing","SetMaxKeyFrameSpacing method [windows Media Format]","SetMaxKeyFrameSpacing method [windows Media Format]","IWMVideoMediaProps interface","wmformat.iwmvideomediaprops_setmaxkeyframespacing","wmsdkidl/IWMVideoMediaProps::SetMaxKeyFrameSpacing"]
old-location: wmformat\iwmvideomediaprops_setmaxkeyframespacing.htm
tech.root: wmformat
ms.assetid: 1d1a9090-2658-45bd-8893-30e063d10aa8
ms.date: 4/26/2023
ms.keywords: IWMVideoMediaProps interface [windows Media Format],SetMaxKeyFrameSpacing method, IWMVideoMediaProps.SetMaxKeyFrameSpacing, IWMVideoMediaProps::SetMaxKeyFrameSpacing, IWMVideoMediaPropsSetMaxKeyFrameSpacing, SetMaxKeyFrameSpacing, SetMaxKeyFrameSpacing method [windows Media Format], SetMaxKeyFrameSpacing method [windows Media Format],IWMVideoMediaProps interface, wmformat.iwmvideomediaprops_setmaxkeyframespacing, wmsdkidl/IWMVideoMediaProps::SetMaxKeyFrameSpacing
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMVideoMediaProps::SetMaxKeyFrameSpacing
 - wmsdkidl/IWMVideoMediaProps::SetMaxKeyFrameSpacing
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
api_name:
 - IWMVideoMediaProps.SetMaxKeyFrameSpacing
---

# IWMVideoMediaProps::SetMaxKeyFrameSpacing


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetMaxKeyFrameSpacing</b> method specifies the maximum interval between key frames.

## -parameters

### -param llTime [in]

Maximum key-frame spacing in 100-nanosecond units.

## -returns

This method always returns S_OK.

## -remarks

A key frame is a video frame that can be rendered without any information being required from any previous frame. A delta frame is a frame that is dependent on a previous frame. The application can seek to a key frame, but not to a delta frame. The SDK does not enforce any limit on the time between key frames. In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally. For recommended values, see <a href="/windows/desktop/wmformat/configuring-video-streams-for-seeking-performance">Configuring Video Streams for Seeking Performance</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmvideomediaprops">IWMVideoMediaProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-getmaxkeyframespacing">IWMVideoMediaProps::GetMaxKeyFrameSpacing</a>