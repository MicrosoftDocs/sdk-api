---
UID: NF:vmr9.IVMRMixerControl9.SetMixingPrefs
title: IVMRMixerControl9::SetMixingPrefs (vmr9.h)
description: The SetMixingPrefs method sets the mixing preferences for the stream.
helpviewer_keywords: ["IVMRMixerControl9 interface [DirectShow]","SetMixingPrefs method","IVMRMixerControl9.SetMixingPrefs","IVMRMixerControl9::SetMixingPrefs","IVMRMixerControl9SetMixingPrefs","SetMixingPrefs","SetMixingPrefs method [DirectShow]","SetMixingPrefs method [DirectShow]","IVMRMixerControl9 interface","dshow.ivmrmixercontrol9_setmixingprefs","vmr9/IVMRMixerControl9::SetMixingPrefs"]
old-location: dshow\ivmrmixercontrol9_setmixingprefs.htm
tech.root: dshow
ms.assetid: db5bf775-685c-4137-846d-fe71cddce08d
ms.date: 4/26/2023
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetMixingPrefs method, IVMRMixerControl9.SetMixingPrefs, IVMRMixerControl9::SetMixingPrefs, IVMRMixerControl9SetMixingPrefs, SetMixingPrefs, SetMixingPrefs method [DirectShow], SetMixingPrefs method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setmixingprefs, vmr9/IVMRMixerControl9::SetMixingPrefs
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRMixerControl9::SetMixingPrefs
 - vmr9/IVMRMixerControl9::SetMixingPrefs
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
 - IVMRMixerControl9.SetMixingPrefs
---

# IVMRMixerControl9::SetMixingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetMixingPrefs</code> method sets the mixing preferences for the stream.

## -parameters

### -param dwMixerPrefs [in]

Bitwise OR combination of <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9mixerprefs">VMR9MixerPrefs</a> flags.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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

The flags for the mixing preferences are divided into three groups: decimation, filtering, and render target. The VMR9MixerPrefs enumeration defines bitmasks to isolate these flags:

<ul>
<li>MixerPref9_DecimateMask</li>
<li>MixerPref9_FilteringMask</li>
<li>MixerPref9_RenderTargetMask</li>
</ul>
You must specify a valid flag for each group. If you want to change a single flag, you can get the current preferences, remove the flag you don't want, and add the flag you want. For example:


```cpp

// Get the current mixing preferences.
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  

// Remove the current render target flag.
dwPrefs &= ~MixerPref_RenderTargetMask; 

// Add the render target flag that we want.
dwPrefs |= MixerPref_RenderTargetYUV;

// Set the new flags.
pMixControl->SetMixingPrefs(dwPrefs);

```


If the VMR is in renderless mode, you must set the allocator-presenter before calling <code>SetMixingPrefs</code>. Otherwise, the VMR cannot determine the capabilities of the Direct3D device.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>