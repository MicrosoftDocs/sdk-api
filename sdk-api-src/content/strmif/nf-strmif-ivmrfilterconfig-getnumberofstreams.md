---
UID: NF:strmif.IVMRFilterConfig.GetNumberOfStreams
title: IVMRFilterConfig::GetNumberOfStreams (strmif.h)
description: The GetNumberOfStreams method retrieves the number of input streams being mixed.
helpviewer_keywords: ["GetNumberOfStreams","GetNumberOfStreams method [DirectShow]","GetNumberOfStreams method [DirectShow]","IVMRFilterConfig interface","IVMRFilterConfig interface [DirectShow]","GetNumberOfStreams method","IVMRFilterConfig.GetNumberOfStreams","IVMRFilterConfig::GetNumberOfStreams","IVMRFilterConfigGetNumberOfStreams","dshow.ivmrfilterconfig_getnumberofstreams","strmif/IVMRFilterConfig::GetNumberOfStreams"]
old-location: dshow\ivmrfilterconfig_getnumberofstreams.htm
tech.root: dshow
ms.assetid: e031c427-23bb-4243-bb38-0837a6db8c2c
ms.date: 4/26/2023
ms.keywords: GetNumberOfStreams, GetNumberOfStreams method [DirectShow], GetNumberOfStreams method [DirectShow],IVMRFilterConfig interface, IVMRFilterConfig interface [DirectShow],GetNumberOfStreams method, IVMRFilterConfig.GetNumberOfStreams, IVMRFilterConfig::GetNumberOfStreams, IVMRFilterConfigGetNumberOfStreams, dshow.ivmrfilterconfig_getnumberofstreams, strmif/IVMRFilterConfig::GetNumberOfStreams
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IVMRFilterConfig::GetNumberOfStreams
 - strmif/IVMRFilterConfig::GetNumberOfStreams
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
 - IVMRFilterConfig.GetNumberOfStreams
---

# IVMRFilterConfig::GetNumberOfStreams


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetNumberOfStreams</code> method retrieves the number of input streams being mixed.

## -parameters

### -param pdwMaxStreams [out]

Pointer to a double word that receives the number of streams being mixed, which is equal to the number of input pins on the VMR.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwMaxStreams</i> is invalid

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrfilterconfig">IVMRFilterConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams">IVMRFilterConfig::SetNumberOfStreams</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>