---
UID: NF:strmif.IVMRWindowlessControl.GetAspectRatioMode
title: IVMRWindowlessControl::GetAspectRatioMode (strmif.h)
description: The GetAspectRatioMode method queries whether the VMR will preserve the aspect ratio of the source video. (IVMRWindowlessControl.GetAspectRatioMode)
helpviewer_keywords: ["GetAspectRatioMode","GetAspectRatioMode method [DirectShow]","GetAspectRatioMode method [DirectShow]","IVMRWindowlessControl interface","IVMRWindowlessControl interface [DirectShow]","GetAspectRatioMode method","IVMRWindowlessControl.GetAspectRatioMode","IVMRWindowlessControl::GetAspectRatioMode","IVMRWindowlessControlGetAspectRatioMode","dshow.ivmrwindowlesscontrol_getaspectratiomode","strmif/IVMRWindowlessControl::GetAspectRatioMode"]
old-location: dshow\ivmrwindowlesscontrol_getaspectratiomode.htm
tech.root: dshow
ms.assetid: 452837f9-e910-4e6b-8552-9da29a6b63f1
ms.date: 12/05/2018
ms.keywords: GetAspectRatioMode, GetAspectRatioMode method [DirectShow], GetAspectRatioMode method [DirectShow],IVMRWindowlessControl interface, IVMRWindowlessControl interface [DirectShow],GetAspectRatioMode method, IVMRWindowlessControl.GetAspectRatioMode, IVMRWindowlessControl::GetAspectRatioMode, IVMRWindowlessControlGetAspectRatioMode, dshow.ivmrwindowlesscontrol_getaspectratiomode, strmif/IVMRWindowlessControl::GetAspectRatioMode
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
 - IVMRWindowlessControl::GetAspectRatioMode
 - strmif/IVMRWindowlessControl::GetAspectRatioMode
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
 - IVMRWindowlessControl.GetAspectRatioMode
---

# IVMRWindowlessControl::GetAspectRatioMode


## -description

The <code>GetAspectRatioMode</code> method queries whether the VMR will preserve the aspect ratio of the source video.

## -parameters

### -param lpAspectRatioMode [out]

Pointer to a variable that receives a <a href="/windows/desktop/api/strmif/ne-strmif-vmr_aspect_ratio_mode">VMR_ASPECT_RATIO_MODE</a> value indicating the aspect ratio mode.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode">IVMRWindowlessControl::SetAspectRatioMode</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
