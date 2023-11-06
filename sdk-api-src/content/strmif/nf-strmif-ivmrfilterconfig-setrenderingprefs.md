---
UID: NF:strmif.IVMRFilterConfig.SetRenderingPrefs
title: IVMRFilterConfig::SetRenderingPrefs (strmif.h)
description: The SetRenderingPrefs method sets various application preferences related to video rendering.
helpviewer_keywords: ["IVMRFilterConfig interface [DirectShow]","SetRenderingPrefs method","IVMRFilterConfig.SetRenderingPrefs","IVMRFilterConfig::SetRenderingPrefs","IVMRFilterConfigSetRenderingPrefs","SetRenderingPrefs","SetRenderingPrefs method [DirectShow]","SetRenderingPrefs method [DirectShow]","IVMRFilterConfig interface","dshow.ivmrfilterconfig_setrenderingprefs","strmif/IVMRFilterConfig::SetRenderingPrefs"]
old-location: dshow\ivmrfilterconfig_setrenderingprefs.htm
tech.root: dshow
ms.assetid: 1374d071-f396-4fcb-8ca2-ac3986960207
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig interface [DirectShow],SetRenderingPrefs method, IVMRFilterConfig.SetRenderingPrefs, IVMRFilterConfig::SetRenderingPrefs, IVMRFilterConfigSetRenderingPrefs, SetRenderingPrefs, SetRenderingPrefs method [DirectShow], SetRenderingPrefs method [DirectShow],IVMRFilterConfig interface, dshow.ivmrfilterconfig_setrenderingprefs, strmif/IVMRFilterConfig::SetRenderingPrefs
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
 - IVMRFilterConfig::SetRenderingPrefs
 - strmif/IVMRFilterConfig::SetRenderingPrefs
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
 - IVMRFilterConfig.SetRenderingPrefs
---

# IVMRFilterConfig::SetRenderingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetRenderingPrefs</code> method sets various application preferences related to video rendering.

## -parameters

### -param dwRenderFlags [in]

Double word containing a bitwise OR of <a href="/windows/desktop/api/strmif/ne-strmif-vmrrenderprefs">VMRRenderPrefs</a> values specifying the rendering preferences.

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
No allocator-presenter is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwRenderFlags</i> is invalid.

</td>
</tr>
</table>

## -remarks

This method calls through to the allocator-presenter's <a href="/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenterconfig-setrenderingprefs">IVMRImagePresenterConfig::SetRenderingPrefs</a> method. (The default allocator-presenter exposes <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenterconfig">IVMRImagePresenterConfig</a>. Custom allocator-presenters can also expose this interface if desired.) If the VMR-7 has not yet created the default allocator-presenter, or if the application provided a custom allocator-presenter which does not support <b>IVMRImagePresenterConfig</b>, this method returns VFW_E_WRONG_STATE. To create the default allocator-presenter, call <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingmode">IVMRFilterConfig::SetRenderingMode</a> with the value VMRMode_Windowed or VMRMode_Windowed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrfilterconfig">IVMRFilterConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-getrenderingprefs">IVMRFilterConfig::GetRenderingPrefs</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>