---
UID: NF:vmr9.IVMRMixerControl9.GetMixingPrefs
title: IVMRMixerControl9::GetMixingPrefs (vmr9.h)
description: The GetMixingPrefs method retrieves the mixing preferences for the stream.
helpviewer_keywords: ["GetMixingPrefs","GetMixingPrefs method [DirectShow]","GetMixingPrefs method [DirectShow]","IVMRMixerControl9 interface","IVMRMixerControl9 interface [DirectShow]","GetMixingPrefs method","IVMRMixerControl9.GetMixingPrefs","IVMRMixerControl9::GetMixingPrefs","IVMRMixerControl9GetMixingPrefs","dshow.ivmrmixercontrol9_getmixingprefs","vmr9/IVMRMixerControl9::GetMixingPrefs"]
old-location: dshow\ivmrmixercontrol9_getmixingprefs.htm
tech.root: dshow
ms.assetid: 25df0310-124a-48a5-b0fc-bea1dfd35781
ms.date: 4/26/2023
ms.keywords: GetMixingPrefs, GetMixingPrefs method [DirectShow], GetMixingPrefs method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetMixingPrefs method, IVMRMixerControl9.GetMixingPrefs, IVMRMixerControl9::GetMixingPrefs, IVMRMixerControl9GetMixingPrefs, dshow.ivmrmixercontrol9_getmixingprefs, vmr9/IVMRMixerControl9::GetMixingPrefs
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
 - IVMRMixerControl9::GetMixingPrefs
 - vmr9/IVMRMixerControl9::GetMixingPrefs
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
 - IVMRMixerControl9.GetMixingPrefs
---

# IVMRMixerControl9::GetMixingPrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMixingPrefs</code> method retrieves the mixing preferences for the stream.

## -parameters

### -param pdwMixerPrefs [out]

Address of a variable that receives a bitwise OR combination of <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9mixerprefs">VMR9MixerPrefs</a> flags.

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

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>