---
UID: NF:vmr9.IVMRAspectRatioControl9.SetAspectRatioMode
title: IVMRAspectRatioControl9::SetAspectRatioMode (vmr9.h)
description: The SetAspectRatioMode method specifies whether the VMR preserves the aspect ratio of the source video.
helpviewer_keywords: ["IVMRAspectRatioControl9 interface [DirectShow]","SetAspectRatioMode method","IVMRAspectRatioControl9.SetAspectRatioMode","IVMRAspectRatioControl9::SetAspectRatioMode","IVMRAspectRatioControl9SetAspectRatioMode","SetAspectRatioMode","SetAspectRatioMode method [DirectShow]","SetAspectRatioMode method [DirectShow]","IVMRAspectRatioControl9 interface","dshow.ivmraspectratiocontrol9_setaspectratiomode","vmr9/IVMRAspectRatioControl9::SetAspectRatioMode"]
old-location: dshow\ivmraspectratiocontrol9_setaspectratiomode.htm
tech.root: dshow
ms.assetid: adc34013-a349-4cf6-b5c2-58b7b212d630
ms.date: 12/05/2018
ms.keywords: IVMRAspectRatioControl9 interface [DirectShow],SetAspectRatioMode method, IVMRAspectRatioControl9.SetAspectRatioMode, IVMRAspectRatioControl9::SetAspectRatioMode, IVMRAspectRatioControl9SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRAspectRatioControl9 interface, dshow.ivmraspectratiocontrol9_setaspectratiomode, vmr9/IVMRAspectRatioControl9::SetAspectRatioMode
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVMRAspectRatioControl9::SetAspectRatioMode
 - vmr9/IVMRAspectRatioControl9::SetAspectRatioMode
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
 - IVMRAspectRatioControl9.SetAspectRatioMode
---

# IVMRAspectRatioControl9::SetAspectRatioMode


## -description

The <code>SetAspectRatioMode</code> method specifies whether the VMR preserves the aspect ratio of the source video.

## -parameters

### -param dwARMode [in]

Specifies a member of the <a href="/windows/desktop/api/strmif/ne-strmif-vmr_aspect_ratio_mode">VMR_ASPECT_RATIO_MODE</a> enumeration type.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

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



<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmraspectratiocontrol9">IVMRAspectRatioControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>