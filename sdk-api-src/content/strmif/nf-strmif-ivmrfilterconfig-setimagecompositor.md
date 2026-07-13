---
UID: NF:strmif.IVMRFilterConfig.SetImageCompositor
title: IVMRFilterConfig::SetImageCompositor (strmif.h)
description: The SetImageCompositor method installs an application-provided image compositor.
helpviewer_keywords: ["IVMRFilterConfig interface [DirectShow]","SetImageCompositor method","IVMRFilterConfig.SetImageCompositor","IVMRFilterConfig::SetImageCompositor","IVMRFilterConfigSetImageCompositor","SetImageCompositor","SetImageCompositor method [DirectShow]","SetImageCompositor method [DirectShow]","IVMRFilterConfig interface","dshow.ivmrfilterconfig_setimagecompositor","strmif/IVMRFilterConfig::SetImageCompositor"]
old-location: dshow\ivmrfilterconfig_setimagecompositor.htm
tech.root: dshow
ms.assetid: 504380d4-4df6-4b01-8db3-5c769a3d4106
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig interface [DirectShow],SetImageCompositor method, IVMRFilterConfig.SetImageCompositor, IVMRFilterConfig::SetImageCompositor, IVMRFilterConfigSetImageCompositor, SetImageCompositor, SetImageCompositor method [DirectShow], SetImageCompositor method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setimagecompositor, strmif/IVMRFilterConfig::SetImageCompositor
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
 - IVMRFilterConfig::SetImageCompositor
 - strmif/IVMRFilterConfig::SetImageCompositor
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
 - IVMRFilterConfig.SetImageCompositor
---

# IVMRFilterConfig::SetImageCompositor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetImageCompositor</code> method installs an application-provided image compositor.

## -parameters

### -param lpVMRImgCompositor [in]

Pointer to the image compositor's <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor</a> interface.

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
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The mixer is not currently loaded.

</td>
</tr>
</table>

## -remarks

Use this method to replace the VMR's default compositor with a custom compositor provided by the application. The image compositor is a sub-component of the mixer.

The compositor is automatically loaded when the VMR is in windowless or windowed mode. When the VMR is in renderless mode, the compositor must be loaded by calling <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams">IVMRFilterConfig::SetNumberOfStreams</a>. The VMR manages all reference counting on the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor</a> interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrfilterconfig">IVMRFilterConfig Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>