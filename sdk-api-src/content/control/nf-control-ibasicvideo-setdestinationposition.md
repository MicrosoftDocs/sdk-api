---
UID: NF:control.IBasicVideo.SetDestinationPosition
title: IBasicVideo::SetDestinationPosition (control.h)
description: The SetDestinationPosition method sets the destination rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","SetDestinationPosition method","IBasicVideo.SetDestinationPosition","IBasicVideo::SetDestinationPosition","IBasicVideoSetDestinationPosition","SetDestinationPosition","SetDestinationPosition method [DirectShow]","SetDestinationPosition method [DirectShow]","IBasicVideo interface","control/IBasicVideo::SetDestinationPosition","dshow.ibasicvideo_setdestinationposition"]
old-location: dshow\ibasicvideo_setdestinationposition.htm
tech.root: dshow
ms.assetid: e638eb33-5a7f-4ebc-910f-72566e251f17
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],SetDestinationPosition method, IBasicVideo.SetDestinationPosition, IBasicVideo::SetDestinationPosition, IBasicVideoSetDestinationPosition, SetDestinationPosition, SetDestinationPosition method [DirectShow], SetDestinationPosition method [DirectShow],IBasicVideo interface, control/IBasicVideo::SetDestinationPosition, dshow.ibasicvideo_setdestinationposition
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
 - IBasicVideo::SetDestinationPosition
 - control/IBasicVideo::SetDestinationPosition
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
 - IBasicVideo.SetDestinationPosition
---

# IBasicVideo::SetDestinationPosition


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDestinationPosition</code> method sets the destination rectangle.

## -parameters

### -param Left [in]

Specifies the x-coordinate, in pixels.

### -param Top [in]

Specifies the y-coordinate, in pixels.

### -param Width [in]

Specifies the width, in pixels.

### -param Height [in]

Specifies the height, in pixels.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. <i>Width</i> and <i>Height</i> must be larger than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer is not connected.

</td>
</tr>
</table>

## -remarks

This method has the same effect as individually calling the <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationleft">IBasicVideo::put_DestinationLeft</a>, <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationtop">IBasicVideo::put_DestinationTop</a>, <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationwidth">IBasicVideo::put_DestinationWidth</a>, and <a href="/windows/desktop/api/control/nf-control-ibasicvideo-put_destinationheight">IBasicVideo::put_DestinationHeight</a> methods.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>