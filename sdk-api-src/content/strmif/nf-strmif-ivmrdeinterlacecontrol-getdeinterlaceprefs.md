---
UID: NF:strmif.IVMRDeinterlaceControl.GetDeinterlacePrefs
title: IVMRDeinterlaceControl::GetDeinterlacePrefs (strmif.h)
description: The GetDeinterlacePrefs method queries how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.
helpviewer_keywords: ["GetDeinterlacePrefs","GetDeinterlacePrefs method [DirectShow]","GetDeinterlacePrefs method [DirectShow]","IVMRDeinterlaceControl interface","IVMRDeinterlaceControl interface [DirectShow]","GetDeinterlacePrefs method","IVMRDeinterlaceControl.GetDeinterlacePrefs","IVMRDeinterlaceControl::GetDeinterlacePrefs","IVMRDeinterlaceControlGetDeinterlacePrefs","dshow.ivmrdeinterlacecontrol_getdeinterlaceprefs","strmif/IVMRDeinterlaceControl::GetDeinterlacePrefs"]
old-location: dshow\ivmrdeinterlacecontrol_getdeinterlaceprefs.htm
tech.root: dshow
ms.assetid: bb9de83c-087e-4d6e-861a-7db388d59a7c
ms.date: 4/26/2023
ms.keywords: GetDeinterlacePrefs, GetDeinterlacePrefs method [DirectShow], GetDeinterlacePrefs method [DirectShow],IVMRDeinterlaceControl interface, IVMRDeinterlaceControl interface [DirectShow],GetDeinterlacePrefs method, IVMRDeinterlaceControl.GetDeinterlacePrefs, IVMRDeinterlaceControl::GetDeinterlacePrefs, IVMRDeinterlaceControlGetDeinterlacePrefs, dshow.ivmrdeinterlacecontrol_getdeinterlaceprefs, strmif/IVMRDeinterlaceControl::GetDeinterlacePrefs
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
 - IVMRDeinterlaceControl::GetDeinterlacePrefs
 - strmif/IVMRDeinterlaceControl::GetDeinterlacePrefs
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
 - IVMRDeinterlaceControl.GetDeinterlacePrefs
---

# IVMRDeinterlaceControl::GetDeinterlacePrefs


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDeinterlacePrefs</b> method queries how the VMR will select a deinterlacing mode if it cannot use the preferred deinterlacing mode.

## -parameters

### -param lpdwDeinterlacePrefs [in]

Pointer to a variable that receives a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vmrdeinterlaceprefs">VMRDeinterlacePrefs</a> enumeration.

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
<dt><b>VFW_E_VMR_NOT_IN_MIXER_MODE</b></dt>
</dl>
</td>
<td width="60%">
The VMR is not in mixer mode.

</td>
</tr>
</table>

## -remarks

By default, the preferred deinterlacing mode is the first mode reported by the driver. The application can set the preferred mode by calling the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlacemode">IVMRDeinterlaceControl::SetDeinterlaceMode</a> method. If the VMR cannot use the preferred mode, it will fall back to another mode as specified by the <i>dwDeinterlacePrefs</i> parameter.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrdeinterlacecontrol">IVMRDeinterlaceControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrdeinterlacecontrol-setdeinterlaceprefs">IVMRDeinterlaceControl::SetDeinterlacePrefs</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>