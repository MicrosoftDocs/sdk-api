---
UID: NF:strmif.IVMRWindowlessControl.SetVideoPosition
title: IVMRWindowlessControl::SetVideoPosition (strmif.h)
description: The SetVideoPosition method sets the source and destination rectangles for the video.
helpviewer_keywords: ["IVMRWindowlessControl interface [DirectShow]","SetVideoPosition method","IVMRWindowlessControl.SetVideoPosition","IVMRWindowlessControl::SetVideoPosition","IVMRWindowlessControlSetVideoPosition","SetVideoPosition","SetVideoPosition method [DirectShow]","SetVideoPosition method [DirectShow]","IVMRWindowlessControl interface","dshow.ivmrwindowlesscontrol_setvideoposition","strmif/IVMRWindowlessControl::SetVideoPosition"]
old-location: dshow\ivmrwindowlesscontrol_setvideoposition.htm
tech.root: dshow
ms.assetid: 3cf75b8e-850d-4514-9502-a71c801e0d92
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetVideoPosition method, IVMRWindowlessControl.SetVideoPosition, IVMRWindowlessControl::SetVideoPosition, IVMRWindowlessControlSetVideoPosition, SetVideoPosition, SetVideoPosition method [DirectShow], SetVideoPosition method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setvideoposition, strmif/IVMRWindowlessControl::SetVideoPosition
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
 - IVMRWindowlessControl::SetVideoPosition
 - strmif/IVMRWindowlessControl::SetVideoPosition
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
 - IVMRWindowlessControl.SetVideoPosition
---

# IVMRWindowlessControl::SetVideoPosition


## -description

The <code>SetVideoPosition</code> method sets the source and destination rectangles for the video.

## -parameters

### -param lpSRCRect [in]

Pointer to a <b>RECT</b> structure that specifies the source rectangle. If <b>NULL</b>, the source rectangle does not change. The default source rectangle is the entire video image.

### -param lpDSTRect [in]

Pointer to a <b>RECT</b> structure that specifies the destination rectangle. If <b>NULL</b>, the destination rectangle does not change. The default destination rectangle is {0, 0, 0, 0}.

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



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-getvideoposition">IVMRWindowlessControl::GetVideoPosition</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>