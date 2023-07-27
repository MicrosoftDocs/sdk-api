---
UID: NF:strmif.IVMRDeinterlaceControl.GetNumberOfDeinterlaceModes
title: IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes (strmif.h)
description: The GetNumberOfDeinterlaceModes method retrieves the deinterlacing modes available to the VMR for the specified video format.
helpviewer_keywords: ["GetNumberOfDeinterlaceModes","GetNumberOfDeinterlaceModes method [DirectShow]","GetNumberOfDeinterlaceModes method [DirectShow]","IVMRDeinterlaceControl interface","IVMRDeinterlaceControl interface [DirectShow]","GetNumberOfDeinterlaceModes method","IVMRDeinterlaceControl.GetNumberOfDeinterlaceModes","IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes","IVMRDeinterlaceControlGetNumberOfDeinterlaceModes","dshow.ivmrdeinterlacecontrol_getnumberofdeinterlacemodes","strmif/IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes"]
old-location: dshow\ivmrdeinterlacecontrol_getnumberofdeinterlacemodes.htm
tech.root: dshow
ms.assetid: 0e6abb00-95fb-453d-9427-178058b217b8
ms.date: 4/26/2023
ms.keywords: GetNumberOfDeinterlaceModes, GetNumberOfDeinterlaceModes method [DirectShow], GetNumberOfDeinterlaceModes method [DirectShow],IVMRDeinterlaceControl interface, IVMRDeinterlaceControl interface [DirectShow],GetNumberOfDeinterlaceModes method, IVMRDeinterlaceControl.GetNumberOfDeinterlaceModes, IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes, IVMRDeinterlaceControlGetNumberOfDeinterlaceModes, dshow.ivmrdeinterlacecontrol_getnumberofdeinterlacemodes, strmif/IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes
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
 - IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes
 - strmif/IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes
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
 - IVMRDeinterlaceControl.GetNumberOfDeinterlaceModes
---

# IVMRDeinterlaceControl::GetNumberOfDeinterlaceModes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetNumberOfDeinterlaceModes</b> method retrieves the deinterlacing modes available to the VMR for the specified video format.

## -parameters

### -param lpVideoDescription [in]

Pointer to a [VMRVideoDesc](/windows/win32/api/strmif/ns-strmif-vmrvideodesc) structure that describes the video.

### -param lpdwNumDeinterlaceModes [in, out]

Pointer to a <b>DWORD</b> value. On input, this value specifies the size of the array given in <i>lpDeinterlaceModes</i>. On output, it receives number of GUIDs the method copied into the array.

### -param lpDeinterlaceModes [out]

Address of an array allocated by caller. The method fills the array with GUID values. To determine the size of the array that is needed, set this parameter to <b>NULL</b> and check the value returned in <i>lpdwNumDeinterlaceModes</i>.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DDRAW_CAPS_NOT_SUITABLE</b></dt>
</dl>
</td>
<td width="60%">
The video card does not support hardware deinterlacing.

</td>
</tr>
</table>

## -remarks

This method returns an array of GUIDs, where each GUID represents a deinterlacing mode that is supported in hardware by the graphics device driver. The array is sorted by quality, so the first entry represents the best quality, the second entry represents the next best quality, and so forth.

All drivers are required to support the following mode:

<table>
<tr>
<th><b>GUID</b></th>
<th>Description
            </th>
</tr>
<tr>
<td>DXVA_DeinterlaceBobDevice</td>
<td>Bob mode</td>
</tr>
</table>
 

Drivers can support additional modes and should define their own GUIDs to identify them. For each returned mode, call the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getdeinterlacemodecaps">IVMRDeinterlaceControl::GetDeinterlaceModeCaps</a> method to get information about that mode.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>