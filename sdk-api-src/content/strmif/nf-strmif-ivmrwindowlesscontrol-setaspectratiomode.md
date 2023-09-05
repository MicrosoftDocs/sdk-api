---
UID: NF:strmif.IVMRWindowlessControl.SetAspectRatioMode
title: IVMRWindowlessControl::SetAspectRatioMode (strmif.h)
description: The SetAspectRatioMode method specifies whether the VMR will preserve the aspect ratio of the source video. (IVMRWindowlessControl.SetAspectRatioMode)
helpviewer_keywords: ["IVMRWindowlessControl interface [DirectShow]","SetAspectRatioMode method","IVMRWindowlessControl.SetAspectRatioMode","IVMRWindowlessControl::SetAspectRatioMode","IVMRWindowlessControlSetAspectRatioMode","SetAspectRatioMode","SetAspectRatioMode method [DirectShow]","SetAspectRatioMode method [DirectShow]","IVMRWindowlessControl interface","dshow.ivmrwindowlesscontrol_setaspectratiomode","strmif/IVMRWindowlessControl::SetAspectRatioMode"]
old-location: dshow\ivmrwindowlesscontrol_setaspectratiomode.htm
tech.root: dshow
ms.assetid: 421910fb-8007-4347-a57c-6a46b7b733b3
ms.date: 4/26/2023
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetAspectRatioMode method, IVMRWindowlessControl.SetAspectRatioMode, IVMRWindowlessControl::SetAspectRatioMode, IVMRWindowlessControlSetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setaspectratiomode, strmif/IVMRWindowlessControl::SetAspectRatioMode
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
 - IVMRWindowlessControl::SetAspectRatioMode
 - strmif/IVMRWindowlessControl::SetAspectRatioMode
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
 - IVMRWindowlessControl.SetAspectRatioMode
---

# IVMRWindowlessControl::SetAspectRatioMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetAspectRatioMode</code> method specifies whether the VMR will preserve the aspect ratio of the source video.

## -parameters

### -param AspectRatioMode [in]

Specifies a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vmr_aspect_ratio_mode">VMR_ASPECT_RATIO_MODE</a> enumeration type.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following:

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
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
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



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-getaspectratiomode">IVMRWindowlessControl::GetAspectRatioMode</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
