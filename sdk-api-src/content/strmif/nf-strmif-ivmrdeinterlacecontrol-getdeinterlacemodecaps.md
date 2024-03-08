---
UID: NF:strmif.IVMRDeinterlaceControl.GetDeinterlaceModeCaps
title: IVMRDeinterlaceControl::GetDeinterlaceModeCaps (strmif.h)
description: The GetDeinterlaceModeCaps method retrieves the capabilities of a specific deinterlacing mode supported by the graphics device driver.
helpviewer_keywords: ["GetDeinterlaceModeCaps","GetDeinterlaceModeCaps method [DirectShow]","GetDeinterlaceModeCaps method [DirectShow]","IVMRDeinterlaceControl interface","IVMRDeinterlaceControl interface [DirectShow]","GetDeinterlaceModeCaps method","IVMRDeinterlaceControl.GetDeinterlaceModeCaps","IVMRDeinterlaceControl::GetDeinterlaceModeCaps","IVMRDeinterlaceControlGetDeinterlaceModeCaps","dshow.ivmrdeinterlacecontrol_getdeinterlacemodecaps","strmif/IVMRDeinterlaceControl::GetDeinterlaceModeCaps"]
old-location: dshow\ivmrdeinterlacecontrol_getdeinterlacemodecaps.htm
tech.root: dshow
ms.assetid: e672f3d4-1009-4c4c-bb1a-08f78c128423
ms.date: 4/26/2023
ms.keywords: GetDeinterlaceModeCaps, GetDeinterlaceModeCaps method [DirectShow], GetDeinterlaceModeCaps method [DirectShow],IVMRDeinterlaceControl interface, IVMRDeinterlaceControl interface [DirectShow],GetDeinterlaceModeCaps method, IVMRDeinterlaceControl.GetDeinterlaceModeCaps, IVMRDeinterlaceControl::GetDeinterlaceModeCaps, IVMRDeinterlaceControlGetDeinterlaceModeCaps, dshow.ivmrdeinterlacecontrol_getdeinterlacemodecaps, strmif/IVMRDeinterlaceControl::GetDeinterlaceModeCaps
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
 - IVMRDeinterlaceControl::GetDeinterlaceModeCaps
 - strmif/IVMRDeinterlaceControl::GetDeinterlaceModeCaps
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
 - IVMRDeinterlaceControl.GetDeinterlaceModeCaps
---

# IVMRDeinterlaceControl::GetDeinterlaceModeCaps


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDeinterlaceModeCaps</b> method retrieves the capabilities of a specific deinterlacing mode supported by the graphics device driver.

## -parameters

### -param lpDeinterlaceMode [in]

Pointer to a GUID that identifies the deinterlacing mode. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-getnumberofdeinterlacemodes">GetNumberOfDeinterlaceModes</a> method to obtain a list of GUIDs supported by the driver.

### -param lpVideoDescription [in]

Pointer to a [VMRVideoDesc](/windows/win32/api/strmif/ns-strmif-vmrvideodesc) structure describing the video to deinterlace. Set the <b>dwSize</b> member of the structure before calling the method.

### -param lpDeinterlaceCaps [out]

Pointer to a [VMRDeinterlaceCaps](/windows/desktop/api/strmif/ns-strmif-vmrdeinterlacecaps) structure. Set the <b>dwSize</b> member of the structure before calling the method. The method fills the structure with information about the specified deinterlacing mode.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument. 

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_VMR_NO_DEINTERLACE_HW</b></dt>
</dl>
</td>
<td width="60%">
The video card does not support hardware deinterlacing.

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
</table>

## -remarks

The method returns [VMRVideoDesc](/windows/win32/api/strmif/ns-strmif-vmrvideodesc) and [VMRDeinterlaceCaps](/windows/desktop/api/strmif/ns-strmif-vmrdeinterlacecaps) structures.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>