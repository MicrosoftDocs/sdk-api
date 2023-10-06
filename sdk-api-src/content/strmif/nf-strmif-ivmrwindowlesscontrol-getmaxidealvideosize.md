---
UID: NF:strmif.IVMRWindowlessControl.GetMaxIdealVideoSize
title: IVMRWindowlessControl::GetMaxIdealVideoSize (strmif.h)
description: The GetMaxIdealVideoSize method retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.
helpviewer_keywords: ["GetMaxIdealVideoSize","GetMaxIdealVideoSize method [DirectShow]","GetMaxIdealVideoSize method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","GetMaxIdealVideoSize method","IVMRWindowlessControl.GetMaxIdealVideoSize","IVMRWindowlessControl::GetMaxIdealVideoSize","IVMRWindowlessControlGetMaxIdealVideoSize","dshow.ivmrwindowlesscontrol_getmaxidealvideosize","strmif/IVMRWindowlessControl::GetMaxIdealVideoSize"]
old-location: dshow\ivmrwindowlesscontrol_getmaxidealvideosize.htm
tech.root: dshow
ms.assetid: 1cfd8c4e-70e0-4a7e-a47e-4ad0535e5cb2
ms.date: 4/26/2023
ms.keywords: GetMaxIdealVideoSize, GetMaxIdealVideoSize method [DirectShow], GetMaxIdealVideoSize method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetMaxIdealVideoSize method, IVMRWindowlessControl.GetMaxIdealVideoSize, IVMRWindowlessControl::GetMaxIdealVideoSize, IVMRWindowlessControlGetMaxIdealVideoSize, dshow.ivmrwindowlesscontrol_getmaxidealvideosize, strmif/IVMRWindowlessControl::GetMaxIdealVideoSize
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
 - IVMRWindowlessControl::GetMaxIdealVideoSize
 - strmif/IVMRWindowlessControl::GetMaxIdealVideoSize
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
 - IVMRWindowlessControl.GetMaxIdealVideoSize
---

# IVMRWindowlessControl::GetMaxIdealVideoSize


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMaxIdealVideoSize</code> method retrieves the maximum video size that the VMR can display without incurring significant performance or image quality degradation.

## -parameters

### -param lpWidth [out]

Pointer that receives the maximum ideal width.

### -param lpHeight [out]

Pointer that receives the maximum ideal height.

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



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-getminidealvideosize">IVMRWindowlessControl::GetMinIdealVideoSize</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>