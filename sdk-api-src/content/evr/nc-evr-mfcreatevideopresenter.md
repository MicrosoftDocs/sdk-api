---
UID: NC:evr.MFCreateVideoPresenter
title: MFCreateVideoPresenter (evr.h)
description: Creates the default video presenter for the enhanced video renderer (EVR).
helpviewer_keywords: ["04a1ce0d-f1ed-4b8a-827c-600297660442","MFCreateVideoPresenter","MFCreateVideoPresenter callback","MFCreateVideoPresenter callback function [Media Foundation]","evr/MFCreateVideoPresenter","mf.mfcreatevideopresenter"]
old-location: mf\mfcreatevideopresenter.htm
tech.root: mfarchive
ms.assetid: 04a1ce0d-f1ed-4b8a-827c-600297660442
ms.date: 12/05/2018
ms.keywords: 04a1ce0d-f1ed-4b8a-827c-600297660442, MFCreateVideoPresenter, MFCreateVideoPresenter callback, MFCreateVideoPresenter callback function [Media Foundation], evr/MFCreateVideoPresenter, mf.mfcreatevideopresenter
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateVideoPresenter
 - evr/MFCreateVideoPresenter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evr.h
api_name:
 - MFCreateVideoPresenter
archived: true
---

## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Creates the default video presenter for the enhanced video renderer (EVR).

## -parameters

### -param pOwner [in]

Pointer to the owner of the object. If the object is aggregated, pass a pointer to the aggregating object's <b>IUnknown</b> interface. Otherwise, set this parameter to <b>NULL</b>.

### -param riidDevice [in]

Interface identifier (IID) of the video device interface that will be used for processing the video. Currently the only supported value is IID_IDirect3DDevice9.

### -param riid [in]

IID of the requested interface on the video presenter. The video presenter exposes the <a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter">IMFVideoPresenter</a> interface.

### -param ppVideoPresenter

Receives a pointer to the requested interface on the video presenter. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>