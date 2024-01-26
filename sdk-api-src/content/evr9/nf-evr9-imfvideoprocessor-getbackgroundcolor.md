---
UID: NF:evr9.IMFVideoProcessor.GetBackgroundColor
title: IMFVideoProcessor::GetBackgroundColor (evr9.h)
description: Retrieves the background color for the composition rectangle. The background color is used for letterboxing the video image.
helpviewer_keywords: ["GetBackgroundColor","GetBackgroundColor method [Media Foundation]","GetBackgroundColor method [Media Foundation]","IMFVideoProcessor interface","IMFVideoProcessor interface [Media Foundation]","GetBackgroundColor method","IMFVideoProcessor.GetBackgroundColor","IMFVideoProcessor::GetBackgroundColor","d9068346-f0b3-4361-a56b-2360ecc3b9d9","evr9/IMFVideoProcessor::GetBackgroundColor","mf.imfvideoprocessor_getbackgroundcolor"]
old-location: mf\imfvideoprocessor_getbackgroundcolor.htm
tech.root: mfarchive
ms.assetid: d9068346-f0b3-4361-a56b-2360ecc3b9d9
ms.date: 12/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [Media Foundation], GetBackgroundColor method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetBackgroundColor method, IMFVideoProcessor.GetBackgroundColor, IMFVideoProcessor::GetBackgroundColor, d9068346-f0b3-4361-a56b-2360ecc3b9d9, evr9/IMFVideoProcessor::GetBackgroundColor, mf.imfvideoprocessor_getbackgroundcolor
req.header: evr9.h
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
 - IMFVideoProcessor::GetBackgroundColor
 - evr9/IMFVideoProcessor::GetBackgroundColor
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
 - IMFVideoProcessor.GetBackgroundColor
archived: true
---

# IMFVideoProcessor::GetBackgroundColor


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Retrieves the background color for the composition rectangle. The background color is used for letterboxing the video image.

## -parameters

### -param lpClrBkg [out]

Pointer to a <b>COLORREF</b> value that receives the background color.

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
</table>

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>