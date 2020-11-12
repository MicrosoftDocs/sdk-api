---
UID: NF:control.IBasicVideo.get_AvgTimePerFrame
title: IBasicVideo::get_AvgTimePerFrame (control.h)
description: The get_AvgTimePerFrame method retrieves the average time between successive frames.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","get_AvgTimePerFrame method","IBasicVideo.get_AvgTimePerFrame","IBasicVideo::get_AvgTimePerFrame","IBasicVideoget_AvgTimePerFrame","control/IBasicVideo::get_AvgTimePerFrame","dshow.ibasicvideo_get_avgtimeperframe","get_AvgTimePerFrame","get_AvgTimePerFrame method [DirectShow]","get_AvgTimePerFrame method [DirectShow]","IBasicVideo interface"]
old-location: dshow\ibasicvideo_get_avgtimeperframe.htm
tech.root: dshow
ms.assetid: a32a1a46-cde3-401a-b933-c72e399e9ea1
ms.date: 12/05/2018
ms.keywords: IBasicVideo interface [DirectShow],get_AvgTimePerFrame method, IBasicVideo.get_AvgTimePerFrame, IBasicVideo::get_AvgTimePerFrame, IBasicVideoget_AvgTimePerFrame, control/IBasicVideo::get_AvgTimePerFrame, dshow.ibasicvideo_get_avgtimeperframe, get_AvgTimePerFrame, get_AvgTimePerFrame method [DirectShow], get_AvgTimePerFrame method [DirectShow],IBasicVideo interface
req.header: control.h
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
 - IBasicVideo::get_AvgTimePerFrame
 - control/IBasicVideo::get_AvgTimePerFrame
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
 - IBasicVideo.get_AvgTimePerFrame
---

# IBasicVideo::get_AvgTimePerFrame


## -description

The <code>get_AvgTimePerFrame</code> method retrieves the average time between successive frames.

## -parameters

### -param pAvgTimePerFrame [out]

Pointer to a variable of type <a href="/windows/desktop/DirectShow/reftime">REFTIME</a> that receives the average frame time, in seconds.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns the authored time per frame. This value is typically set by the source filter, which obtains it from information in the video stream itself. This value is not necessarily equal to the actual time per frame at which the video is rendered.

To retrieve the actual frame rate during playback, use the <a href="/previous-versions/ms786607(v=vs.85)">IQualProp::get_AvgFrameRate</a>. For more information on actual versus authored frame rates, see the Remarks section for the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>