---
UID: NF:strmif.IVMRMixerControl.SetMixingPrefs
title: IVMRMixerControl::SetMixingPrefs (strmif.h)
description: Sets the mixing preferences for the stream.
helpviewer_keywords: ["IVMRMixerControl interface [DirectShow]","SetMixingPrefs method","IVMRMixerControl.SetMixingPrefs","IVMRMixerControl::SetMixingPrefs","IVMRMixerControlSetOutputRect","SetMixingPrefs","SetMixingPrefs method [DirectShow]","SetMixingPrefs method [DirectShow]","IVMRMixerControl interface","dshow.ivmrmixercontrol_setmixingprefs","strmif/IVMRMixerControl::SetMixingPrefs"]
old-location: dshow\ivmrmixercontrol_setmixingprefs.htm
tech.root: dshow
ms.assetid: b0bd2086-af22-4530-921d-b7c56471d142
ms.date: 4/26/2023
ms.keywords: IVMRMixerControl interface [DirectShow],SetMixingPrefs method, IVMRMixerControl.SetMixingPrefs, IVMRMixerControl::SetMixingPrefs, IVMRMixerControlSetOutputRect, SetMixingPrefs, SetMixingPrefs method [DirectShow], SetMixingPrefs method [DirectShow],IVMRMixerControl interface, dshow.ivmrmixercontrol_setmixingprefs, strmif/IVMRMixerControl::SetMixingPrefs
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
 - IVMRMixerControl::SetMixingPrefs
 - strmif/IVMRMixerControl::SetMixingPrefs
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
 - IVMRMixerControl.SetMixingPrefs
---

# IVMRMixerControl::SetMixingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Sets the mixing preferences for the stream.

## -parameters

### -param dwMixerPrefs [in]

Bitwise <b>OR</b> combination of <a href="/windows/desktop/api/strmif/ne-strmif-vmrmixerprefs">VMRMixerPrefs</a> flags.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The flags for the mixing preferences are divided into three groups: decimation, filtering, and render target. The VMRMixerPrefs enumeration defines bitmasks to isolate these flags:

<ul>
<li>MixerPref_DecimateMask</li>
<li>MixerPref_FilteringMask</li>
<li>MixerPref_RenderTargetMask</li>
</ul>
You must specify a valid flag for each group. If you want to change a single flag, you can get the current preferences, remove the flag you don't want, and add the flag you want. For example:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Get the current mixing preferences.
DWORD dwPrefs;
pMixControl-&gt;GetMixingPrefs(&amp;dwPrefs);  

// Remove the current render target flag.
dwPrefs &amp;= ~MixerPref_RenderTargetMask; 

// Add the render target flag that we want.
dwPrefs |= MixerPref_RenderTargetYUV;

// Set the new flags.
pMixControl-&gt;SetMixingPrefs(dwPrefs);
</pre>
</td>
</tr>
</table></span></div>
If the VMR is in renderless mode, you must set the allocator-presenter before calling <code>SetMixingPrefs</code>. Otherwise, the VMR cannot determine the capabilities of the Direct3D device.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>