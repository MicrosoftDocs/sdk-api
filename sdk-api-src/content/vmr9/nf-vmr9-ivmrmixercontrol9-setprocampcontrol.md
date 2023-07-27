---
UID: NF:vmr9.IVMRMixerControl9.SetProcAmpControl
title: IVMRMixerControl9::SetProcAmpControl (vmr9.h)
description: The SetProcAmpControl method sets the image adjustment for the VMR-9.
helpviewer_keywords: ["IVMRMixerControl9 interface [DirectShow]","SetProcAmpControl method","IVMRMixerControl9.SetProcAmpControl","IVMRMixerControl9::SetProcAmpControl","IVMRMixerControl9SetProcAmpControl","SetProcAmpControl","SetProcAmpControl method [DirectShow]","SetProcAmpControl method [DirectShow]","IVMRMixerControl9 interface","dshow.ivmrmixercontrol9_setprocampcontrol","vmr9/IVMRMixerControl9::SetProcAmpControl"]
old-location: dshow\ivmrmixercontrol9_setprocampcontrol.htm
tech.root: dshow
ms.assetid: 6e2949f5-87e5-4748-bb23-be14452c8c82
ms.date: 4/26/2023
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetProcAmpControl method, IVMRMixerControl9.SetProcAmpControl, IVMRMixerControl9::SetProcAmpControl, IVMRMixerControl9SetProcAmpControl, SetProcAmpControl, SetProcAmpControl method [DirectShow], SetProcAmpControl method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setprocampcontrol, vmr9/IVMRMixerControl9::SetProcAmpControl
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
 - IVMRMixerControl9::SetProcAmpControl
 - vmr9/IVMRMixerControl9::SetProcAmpControl
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
 - IVMRMixerControl9.SetProcAmpControl
---

# IVMRMixerControl9::SetProcAmpControl


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetProcAmpControl</code> method sets the image adjustment for the VMR-9. Image adjustment includes brightness, contrast, hue, and saturation, and is performed by the graphics device. If the graphics driver does not support hardware image adjustment, this method fails.

## -parameters

### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.

### -param lpClrControl [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9procampcontrol">VMR9ProcAmpControl</a> structure that contains the image adjustment settings.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. Possible causes of this error include:

<ul>
<li>The stream number is invalid</li>
<li>The value of <b>dwSize</b> in the <b>VMR9ProcAmpControl</b> structure is invalid.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NO_PROCAMP_HW</b></dt>
</dl>
</td>
<td width="60%">
The graphics hardware does not support ProcAmp controls.

</td>
</tr>
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>