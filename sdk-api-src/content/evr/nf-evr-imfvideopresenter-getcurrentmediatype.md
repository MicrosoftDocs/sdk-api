---
UID: NF:evr.IMFVideoPresenter.GetCurrentMediaType
title: IMFVideoPresenter::GetCurrentMediaType (evr.h)
description: Retrieves the presenter's media type.
helpviewer_keywords: ["4b8f0e56-35de-4b4f-9897-32a7e14171c8","GetCurrentMediaType","GetCurrentMediaType method [Media Foundation]","GetCurrentMediaType method [Media Foundation]","IMFVideoPresenter interface","IMFVideoPresenter interface [Media Foundation]","GetCurrentMediaType method","IMFVideoPresenter.GetCurrentMediaType","IMFVideoPresenter::GetCurrentMediaType","evr/IMFVideoPresenter::GetCurrentMediaType","mf.imfvideopresenter_getcurrentmediatype"]
old-location: mf\imfvideopresenter_getcurrentmediatype.htm
tech.root: mfarchive
ms.assetid: 4b8f0e56-35de-4b4f-9897-32a7e14171c8
ms.date: 12/05/2018
ms.keywords: 4b8f0e56-35de-4b4f-9897-32a7e14171c8, GetCurrentMediaType, GetCurrentMediaType method [Media Foundation], GetCurrentMediaType method [Media Foundation],IMFVideoPresenter interface, IMFVideoPresenter interface [Media Foundation],GetCurrentMediaType method, IMFVideoPresenter.GetCurrentMediaType, IMFVideoPresenter::GetCurrentMediaType, evr/IMFVideoPresenter::GetCurrentMediaType, mf.imfvideopresenter_getcurrentmediatype
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFVideoPresenter::GetCurrentMediaType
 - evr/IMFVideoPresenter::GetCurrentMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPresenter.GetCurrentMediaType
archived: true
---

# IMFVideoPresenter::GetCurrentMediaType


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Retrieves the presenter's media type.

## -parameters

### -param ppMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a> interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The media type is not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down

</td>
</tr>
</table>

## -remarks

This method returns the media type that the presenter sets for the mixer's output type. It describes the format of the composited image.

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter">IMFVideoPresenter</a>