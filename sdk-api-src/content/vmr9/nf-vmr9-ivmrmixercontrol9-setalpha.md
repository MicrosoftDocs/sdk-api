---
UID: NF:vmr9.IVMRMixerControl9.SetAlpha
title: IVMRMixerControl9::SetAlpha (vmr9.h)
description: The SetAlpha method sets a constant alpha value that is applied to this video stream.
helpviewer_keywords: ["IVMRMixerControl9 interface [DirectShow]","SetAlpha method","IVMRMixerControl9.SetAlpha","IVMRMixerControl9::SetAlpha","IVMRMixerControl9SetAlpha","SetAlpha","SetAlpha method [DirectShow]","SetAlpha method [DirectShow]","IVMRMixerControl9 interface","dshow.ivmrmixercontrol9_setalpha","vmr9/IVMRMixerControl9::SetAlpha"]
old-location: dshow\ivmrmixercontrol9_setalpha.htm
tech.root: dshow
ms.assetid: c746d473-bfa4-403c-8775-3f7270836a73
ms.date: 12/05/2018
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetAlpha method, IVMRMixerControl9.SetAlpha, IVMRMixerControl9::SetAlpha, IVMRMixerControl9SetAlpha, SetAlpha, SetAlpha method [DirectShow], SetAlpha method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setalpha, vmr9/IVMRMixerControl9::SetAlpha
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
 - IVMRMixerControl9::SetAlpha
 - vmr9/IVMRMixerControl9::SetAlpha
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
 - IVMRMixerControl9.SetAlpha
---

# IVMRMixerControl9::SetAlpha


## -description

The <code>SetAlpha</code> method sets a constant alpha value that is applied to this video stream.

## -parameters

### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.

### -param Alpha [in]

Specifies the alpha blending value to be applied to all the pixels in this stream.

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
</table>

## -remarks

The alpha value specified can range from 0.0 (fully transparent) to 1.0 (full opaque).

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>