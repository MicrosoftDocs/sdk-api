---
UID: NF:vmr9.IVMRMixerControl9.GetZOrder
title: IVMRMixerControl9::GetZOrder (vmr9.h)
description: The GetZOrder method retrieves this video stream's position in the Z-order.
helpviewer_keywords: ["GetZOrder","GetZOrder method [DirectShow]","GetZOrder method [DirectShow]","IVMRMixerControl9 interface","IVMRMixerControl9 interface [DirectShow]","GetZOrder method","IVMRMixerControl9.GetZOrder","IVMRMixerControl9::GetZOrder","IVMRMixerControl9GetZOrder","dshow.ivmrmixercontrol9_getzorder","vmr9/IVMRMixerControl9::GetZOrder"]
old-location: dshow\ivmrmixercontrol9_getzorder.htm
tech.root: dshow
ms.assetid: eccc72cc-9ae5-45e9-a47a-5dddc901d1b5
ms.date: 4/26/2023
ms.keywords: GetZOrder, GetZOrder method [DirectShow], GetZOrder method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetZOrder method, IVMRMixerControl9.GetZOrder, IVMRMixerControl9::GetZOrder, IVMRMixerControl9GetZOrder, dshow.ivmrmixercontrol9_getzorder, vmr9/IVMRMixerControl9::GetZOrder
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
 - IVMRMixerControl9::GetZOrder
 - vmr9/IVMRMixerControl9::GetZOrder
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
 - IVMRMixerControl9.GetZOrder
---

# IVMRMixerControl9::GetZOrder


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetZOrder</code> method retrieves this video stream's position in the Z-order.

## -parameters

### -param dwStreamID [in]

Specifies the input stream. This value corresponds to the input pin. For example, the first input pin is stream 0.

### -param pZ [out]

Pointer that receives the current position in the Z-order.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pZ</i> is invalid.

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

The default Z-order is the order in which the pins were created.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>