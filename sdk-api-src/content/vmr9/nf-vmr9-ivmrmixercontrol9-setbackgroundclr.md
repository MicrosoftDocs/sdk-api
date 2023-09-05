---
UID: NF:vmr9.IVMRMixerControl9.SetBackgroundClr
title: IVMRMixerControl9::SetBackgroundClr (vmr9.h)
description: The SetBackgroundClr method sets the background color on the output rectangle.
helpviewer_keywords: ["IVMRMixerControl9 interface [DirectShow]","SetBackgroundClr method","IVMRMixerControl9.SetBackgroundClr","IVMRMixerControl9::SetBackgroundClr","IVMRMixerControl9SetBackgroundClr","SetBackgroundClr","SetBackgroundClr method [DirectShow]","SetBackgroundClr method [DirectShow]","IVMRMixerControl9 interface","dshow.ivmrmixercontrol9_setbackgroundclr","vmr9/IVMRMixerControl9::SetBackgroundClr"]
old-location: dshow\ivmrmixercontrol9_setbackgroundclr.htm
tech.root: dshow
ms.assetid: fed7f4bb-519c-4e02-be99-065b9131e57c
ms.date: 4/26/2023
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetBackgroundClr method, IVMRMixerControl9.SetBackgroundClr, IVMRMixerControl9::SetBackgroundClr, IVMRMixerControl9SetBackgroundClr, SetBackgroundClr, SetBackgroundClr method [DirectShow], SetBackgroundClr method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setbackgroundclr, vmr9/IVMRMixerControl9::SetBackgroundClr
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
 - IVMRMixerControl9::SetBackgroundClr
 - vmr9/IVMRMixerControl9::SetBackgroundClr
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
 - IVMRMixerControl9.SetBackgroundClr
---

# IVMRMixerControl9::SetBackgroundClr


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetBackgroundClr</code> method sets the background color on the output rectangle.

## -parameters

### -param ClrBkg [in]

Specifies the background color.

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