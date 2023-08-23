---
UID: NF:strmif.IVMRFilterConfig.GetRenderingPrefs
title: IVMRFilterConfig::GetRenderingPrefs (strmif.h)
description: The GetRenderingPrefs method retrieves the current set of rendering preferences being used by the VMR.
helpviewer_keywords: ["GetRenderingPrefs","GetRenderingPrefs method [DirectShow]","GetRenderingPrefs method [DirectShow]","IVMRFilterConfig interface","IVMRFilterConfig interface [DirectShow]","GetRenderingPrefs method","IVMRFilterConfig.GetRenderingPrefs","IVMRFilterConfig::GetRenderingPrefs","IVMRFilterConfigGetRenderingPrefs","dshow.ivmrfilterconfig_getrenderingprefs","strmif/IVMRFilterConfig::GetRenderingPrefs"]
old-location: dshow\ivmrfilterconfig_getrenderingprefs.htm
tech.root: dshow
ms.assetid: aabf3628-3179-430c-a74b-0cb4e552cbe2
ms.date: 4/26/2023
ms.keywords: GetRenderingPrefs, GetRenderingPrefs method [DirectShow], GetRenderingPrefs method [DirectShow],IVMRFilterConfig interface, IVMRFilterConfig interface [DirectShow],GetRenderingPrefs method, IVMRFilterConfig.GetRenderingPrefs, IVMRFilterConfig::GetRenderingPrefs, IVMRFilterConfigGetRenderingPrefs, dshow.ivmrfilterconfig_getrenderingprefs, strmif/IVMRFilterConfig::GetRenderingPrefs
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
 - IVMRFilterConfig::GetRenderingPrefs
 - strmif/IVMRFilterConfig::GetRenderingPrefs
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
 - IVMRFilterConfig.GetRenderingPrefs
---

# IVMRFilterConfig::GetRenderingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetRenderingPrefs</code> method retrieves the current set of rendering preferences being used by the VMR.

## -parameters

### -param pdwRenderFlags [out]

Receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vmrrenderprefs">VMRRenderPrefs</a> enumeration, indicating the current rendering preferences.

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
<i>pdwRenderingPrefs</i> is invalid

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
No allocator-presenter object is currently loaded.

</td>
</tr>
</table>

## -remarks

This method calls through to the allocator-presenter's <a href="/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenterconfig-getrenderingprefs">IVMRImagePresenterConfig::GetRenderingPrefs</a> method. (The default allocator-presenter exposes <b>IVMRImagePresenterConfig</b>. Custom allocator-presenters can also expose this interface if desired.) If the VMR-7 has not yet created the default allocator-presenter, or if the application provided a custom allocator-presenter which does not support <b>IVMRImagePresenterConfig</b>, this method returns VFW_E_WRONG_STATE. To create the default allocator-presenter, call <a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingmode">IVMRFilterConfig::SetRenderingMode</a> with the value VMRMode_Windowed or VMRMode_Windowed.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrfilterconfig">IVMRFilterConfig Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs">IVMRFilterConfig::SetRenderingPrefs</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>