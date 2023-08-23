---
UID: NF:strmif.IVMRWindowlessControl.GetBorderColor
title: IVMRWindowlessControl::GetBorderColor (strmif.h)
description: The GetBorderColor method retrieves the current border color used by the VMR.
helpviewer_keywords: ["GetBorderColor","GetBorderColor method [DirectShow]","GetBorderColor method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","GetBorderColor method","IVMRWindowlessControl.GetBorderColor","IVMRWindowlessControl::GetBorderColor","IVMRWindowlessControlGetBorderColor","dshow.ivmrwindowlesscontrol_getbordercolor","strmif/IVMRWindowlessControl::GetBorderColor"]
old-location: dshow\ivmrwindowlesscontrol_getbordercolor.htm
tech.root: dshow
ms.assetid: f0bf04c8-17e6-4e1f-b35f-2e10c9de8b92
ms.date: 4/26/2023
ms.keywords: GetBorderColor, GetBorderColor method [DirectShow], GetBorderColor method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetBorderColor method, IVMRWindowlessControl.GetBorderColor, IVMRWindowlessControl::GetBorderColor, IVMRWindowlessControlGetBorderColor, dshow.ivmrwindowlesscontrol_getbordercolor, strmif/IVMRWindowlessControl::GetBorderColor
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
 - IVMRWindowlessControl::GetBorderColor
 - strmif/IVMRWindowlessControl::GetBorderColor
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
 - IVMRWindowlessControl.GetBorderColor
---

# IVMRWindowlessControl::GetBorderColor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetBorderColor</code> method retrieves the current border color used by the VMR.

## -parameters

### -param lpClr [out]

Pointer to a <b>COLORREF</b> variable that receives the current border color.

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
The VMR is not in windowless mode.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-setbordercolor">IVMRWindowlessControl::SetBorderColor</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>