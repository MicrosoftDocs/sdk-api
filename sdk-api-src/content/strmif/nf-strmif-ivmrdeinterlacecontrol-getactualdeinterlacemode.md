---
UID: NF:strmif.IVMRDeinterlaceControl.GetActualDeinterlaceMode
title: IVMRDeinterlaceControl::GetActualDeinterlaceMode (strmif.h)
description: The GetActualDeinterlaceMode method returns the deinterlacing mode that the VMR is using for a specified stream.
helpviewer_keywords: ["GetActualDeinterlaceMode","GetActualDeinterlaceMode method [DirectShow]","GetActualDeinterlaceMode method [DirectShow]","IVMRDeinterlaceControl interface","IVMRDeinterlaceControl interface [DirectShow]","GetActualDeinterlaceMode method","IVMRDeinterlaceControl.GetActualDeinterlaceMode","IVMRDeinterlaceControl::GetActualDeinterlaceMode","IVMRDeinterlaceControlGetActualDeinterlaceMode","dshow.ivmrdeinterlacecontrol_getactualdeinterlacemode","strmif/IVMRDeinterlaceControl::GetActualDeinterlaceMode"]
old-location: dshow\ivmrdeinterlacecontrol_getactualdeinterlacemode.htm
tech.root: dshow
ms.assetid: b8b5c619-68fe-40a5-8621-ef6e9ad612d8
ms.date: 4/26/2023
ms.keywords: GetActualDeinterlaceMode, GetActualDeinterlaceMode method [DirectShow], GetActualDeinterlaceMode method [DirectShow],IVMRDeinterlaceControl interface, IVMRDeinterlaceControl interface [DirectShow],GetActualDeinterlaceMode method, IVMRDeinterlaceControl.GetActualDeinterlaceMode, IVMRDeinterlaceControl::GetActualDeinterlaceMode, IVMRDeinterlaceControlGetActualDeinterlaceMode, dshow.ivmrdeinterlacecontrol_getactualdeinterlacemode, strmif/IVMRDeinterlaceControl::GetActualDeinterlaceMode
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
 - IVMRDeinterlaceControl::GetActualDeinterlaceMode
 - strmif/IVMRDeinterlaceControl::GetActualDeinterlaceMode
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
 - IVMRDeinterlaceControl.GetActualDeinterlaceMode
---

# IVMRDeinterlaceControl::GetActualDeinterlaceMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetActualDeinterlaceMode</b> method returns the deinterlacing mode that the VMR is using for a specified stream.

## -parameters

### -param dwStreamID [in]

Index of the video stream.

### -param lpDeinterlaceMode [out]

Pointer to a variable that receives a GUID value that identifies the deinterlacing mode. The method returns GUID_NULL if the VMR has not initialized the deinterlacing hardware, or if the VMR determines that this stream should not be deinterlaced.

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
Invalid stream number.

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
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>