---
UID: NF:vmr9.IVMRFilterConfig9.SetRenderingMode
title: IVMRFilterConfig9::SetRenderingMode (vmr9.h)
description: The SetRenderingMode method sets the rendering mode used by the VMR.
helpviewer_keywords: ["IVMRFilterConfig9 interface [DirectShow]","SetRenderingMode method","IVMRFilterConfig9.SetRenderingMode","IVMRFilterConfig9::SetRenderingMode","IVMRFilterConfig9SetRenderingMode","SetRenderingMode","SetRenderingMode method [DirectShow]","SetRenderingMode method [DirectShow]","IVMRFilterConfig9 interface","dshow.ivmrfilterconfig9_setrenderingmode","vmr9/IVMRFilterConfig9::SetRenderingMode"]
old-location: dshow\ivmrfilterconfig9_setrenderingmode.htm
tech.root: dshow
ms.assetid: d7a27d7c-5cd4-4a20-ba15-7056d502e3e3
ms.date: 4/26/2023
ms.keywords: IVMRFilterConfig9 interface [DirectShow],SetRenderingMode method, IVMRFilterConfig9.SetRenderingMode, IVMRFilterConfig9::SetRenderingMode, IVMRFilterConfig9SetRenderingMode, SetRenderingMode, SetRenderingMode method [DirectShow], SetRenderingMode method [DirectShow],IVMRFilterConfig9 interface, dshow.ivmrfilterconfig9_setrenderingmode, vmr9/IVMRFilterConfig9::SetRenderingMode
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
 - IVMRFilterConfig9::SetRenderingMode
 - vmr9/IVMRFilterConfig9::SetRenderingMode
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
 - IVMRFilterConfig9.SetRenderingMode
---

# IVMRFilterConfig9::SetRenderingMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetRenderingMode</code> method sets the rendering mode used by the VMR.

## -parameters

### -param Mode [in]

Specifies the rendering mode as a <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9mode">VMR9Mode</a> value.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid rendering mode was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The mode cannot be changed for some reason. See Remarks.

</td>
</tr>
</table>

## -remarks

The VMR is in windowed mode (<b>VMR9Mode_Windowed</b>) by default. Use this method to put the VMR into windowless mode (<b>VMR9Mode_Windowless</b>) or renderless mode (<b>VMR9Mode_Renderless</b>).

The mode cannot be changed after any pin has been connected. Also, the mode cannot be changed from windowless or renderless mode back to windowed mode, even before pins are connected. Therefore, specifying <b>VMR9Mode_Windowed</b> for the <i>Mode</i> parameter has no effect under any circumstances.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="/windows/desktop/DirectShow/vmr-modes-of-operation">VMR Modes of Operation</a>