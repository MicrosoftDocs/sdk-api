---
UID: NF:strmif.IVMRWindowlessControl.GetMinIdealVideoSize
title: IVMRWindowlessControl::GetMinIdealVideoSize (strmif.h)
description: The GetMinIdealVideoSize method retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.
helpviewer_keywords: ["GetMinIdealVideoSize","GetMinIdealVideoSize method [DirectShow]","GetMinIdealVideoSize method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","GetMinIdealVideoSize method","IVMRWindowlessControl.GetMinIdealVideoSize","IVMRWindowlessControl::GetMinIdealVideoSize","IVMRWindowlessControlGetMinIdealVideoSize","dshow.ivmrwindowlesscontrol_getminidealvideosize","strmif/IVMRWindowlessControl::GetMinIdealVideoSize"]
old-location: dshow\ivmrwindowlesscontrol_getminidealvideosize.htm
tech.root: dshow
ms.assetid: 602e32d4-41d6-4139-aa64-4b53caa50859
ms.date: 12/05/2018
ms.keywords: GetMinIdealVideoSize, GetMinIdealVideoSize method [DirectShow], GetMinIdealVideoSize method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetMinIdealVideoSize method, IVMRWindowlessControl.GetMinIdealVideoSize, IVMRWindowlessControl::GetMinIdealVideoSize, IVMRWindowlessControlGetMinIdealVideoSize, dshow.ivmrwindowlesscontrol_getminidealvideosize, strmif/IVMRWindowlessControl::GetMinIdealVideoSize
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
 - IVMRWindowlessControl::GetMinIdealVideoSize
 - strmif/IVMRWindowlessControl::GetMinIdealVideoSize
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
 - IVMRWindowlessControl.GetMinIdealVideoSize
---

# IVMRWindowlessControl::GetMinIdealVideoSize


## -description

The <code>GetMinIdealVideoSize</code> method retrieves the minimum video size that the VMR can display without incurring significant performance or image quality degradation.

## -parameters

### -param lpWidth [out]

Pointer to a LONG value that receives the minimum ideal width.

### -param lpHeight [out]

Pointer to a LONG value that receives the minimum ideal height.

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



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-getmaxidealvideosize">IVMRWindowlessControl::GetMaxIdealVideoSize</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>