---
UID: NF:strmif.IGraphConfig.GetStartTime
title: IGraphConfig::GetStartTime (strmif.h)
description: The GetStartTime method retrieves the reference time that was used when the filter graph was last put into a running state.
helpviewer_keywords: ["GetStartTime","GetStartTime method [DirectShow]","GetStartTime method [DirectShow]","IGraphConfig interface","IGraphConfig interface [DirectShow]","GetStartTime method","IGraphConfig.GetStartTime","IGraphConfig::GetStartTime","IGraphConfigGetStartTime","dshow.igraphconfig_getstarttime","strmif/IGraphConfig::GetStartTime"]
old-location: dshow\igraphconfig_getstarttime.htm
tech.root: dshow
ms.assetid: 76d06517-3029-4ece-934e-b1c6f7f65f2c
ms.date: 4/26/2023
ms.keywords: GetStartTime, GetStartTime method [DirectShow], GetStartTime method [DirectShow],IGraphConfig interface, IGraphConfig interface [DirectShow],GetStartTime method, IGraphConfig.GetStartTime, IGraphConfig::GetStartTime, IGraphConfigGetStartTime, dshow.igraphconfig_getstarttime, strmif/IGraphConfig::GetStartTime
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IGraphConfig::GetStartTime
 - strmif/IGraphConfig::GetStartTime
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
 - IGraphConfig.GetStartTime
---

# IGraphConfig::GetStartTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStartTime</code> method retrieves the reference time that was used when the filter graph was last put into a running state.

## -parameters

### -param prtStart [out]

Receives the start time.

## -returns

Returns one of the following <b>HRESULT</b> values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter graph is not in a running state.

</td>
</tr>
</table>

## -remarks

The filter graph must currently be in a running state or this method will fail.

