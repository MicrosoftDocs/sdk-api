---
UID: NF:strmif.IVMRAspectRatioControl.SetAspectRatioMode
title: IVMRAspectRatioControl::SetAspectRatioMode (strmif.h)
description: The SetAspectRatioMode method specifies whether the VMR will preserve the aspect ratio of the source video.
helpviewer_keywords: ["IVMRAspectRatioControl interface [DirectShow]","SetAspectRatioMode method","IVMRAspectRatioControl.SetAspectRatioMode","IVMRAspectRatioControl::SetAspectRatioMode","IVMRAspectRatioControlSetAspectRatioMode","SetAspectRatioMode","SetAspectRatioMode method [DirectShow]","SetAspectRatioMode method [DirectShow]","IVMRAspectRatioControl interface","dshow.ivmraspectratiocontrol_setaspectratiomode","strmif/IVMRAspectRatioControl::SetAspectRatioMode"]
old-location: dshow\ivmraspectratiocontrol_setaspectratiomode.htm
tech.root: dshow
ms.assetid: e73362ea-b153-4d25-b30e-c69274b49bf9
ms.date: 12/05/2018
ms.keywords: IVMRAspectRatioControl interface [DirectShow],SetAspectRatioMode method, IVMRAspectRatioControl.SetAspectRatioMode, IVMRAspectRatioControl::SetAspectRatioMode, IVMRAspectRatioControlSetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRAspectRatioControl interface, dshow.ivmraspectratiocontrol_setaspectratiomode, strmif/IVMRAspectRatioControl::SetAspectRatioMode
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
 - IVMRAspectRatioControl::SetAspectRatioMode
 - strmif/IVMRAspectRatioControl::SetAspectRatioMode
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
 - IVMRAspectRatioControl.SetAspectRatioMode
---

# IVMRAspectRatioControl::SetAspectRatioMode


## -description

The <code>SetAspectRatioMode</code> method specifies whether the VMR will preserve the aspect ratio of the source video.

## -parameters

### -param dwARMode [in]

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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ivmraspectratiocontrol">IVMRAspectRatioControl Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>