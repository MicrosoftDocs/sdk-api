---
UID: NC:evr.MFCreateVideoRenderer
title: MFCreateVideoRenderer (evr.h)
description: Creates an instance of the enhanced video renderer (EVR) media sink.
helpviewer_keywords: ["MFCreateVideoRenderer","MFCreateVideoRenderer callback","MFCreateVideoRenderer callback function [Media Foundation]","d0f90c42-8f08-44f4-b3da-b9f3ae4869e6","evr/MFCreateVideoRenderer","mf.mfcreatevideorenderer"]
old-location: mf\mfcreatevideorenderer.htm
tech.root: mfarchive
ms.assetid: d0f90c42-8f08-44f4-b3da-b9f3ae4869e6
ms.date: 12/05/2018
ms.keywords: MFCreateVideoRenderer, MFCreateVideoRenderer callback, MFCreateVideoRenderer callback function [Media Foundation], d0f90c42-8f08-44f4-b3da-b9f3ae4869e6, evr/MFCreateVideoRenderer, mf.mfcreatevideorenderer
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
 - MFCreateVideoRenderer
 - evr/MFCreateVideoRenderer
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
 - MFCreateVideoRenderer
archived: true
---

# MFCreateVideoRenderer callback function


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Creates an instance of the enhanced video renderer (EVR) media sink.

## -parameters

### -param riidRenderer [in]

Interface identifier (IID) of the requested interface on the EVR.

### -param ppVideoRenderer [out]

Receives a pointer to the requested interface. The caller must release the interface.

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

## -remarks

This function creates the Media Foundation version of the EVR. To create the DirectShow EVR filter, call <b>CoCreateInstance</b> with the class identifier CLSID_EnhancedVideoRenderer.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>