---
UID: NF:vmr9.IVMRWindowlessControl9.SetAspectRatioMode
title: IVMRWindowlessControl9::SetAspectRatioMode (vmr9.h)
description: The SetAspectRatioMode method sets the current aspect ratio display mode.
helpviewer_keywords: ["IVMRWindowlessControl9 interface [DirectShow]","SetAspectRatioMode method","IVMRWindowlessControl9.SetAspectRatioMode","IVMRWindowlessControl9::SetAspectRatioMode","IVMRWindowlessControl9SetAspectRatioMode","SetAspectRatioMode","SetAspectRatioMode method [DirectShow]","SetAspectRatioMode method [DirectShow]","IVMRWindowlessControl9 interface","dshow.ivmrwindowlesscontrol9_setaspectratiomode","vmr9/IVMRWindowlessControl9::SetAspectRatioMode"]
old-location: dshow\ivmrwindowlesscontrol9_setaspectratiomode.htm
tech.root: dshow
ms.assetid: 5ba46490-0a82-495f-8742-d7a8efa95332
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl9 interface [DirectShow],SetAspectRatioMode method, IVMRWindowlessControl9.SetAspectRatioMode, IVMRWindowlessControl9::SetAspectRatioMode, IVMRWindowlessControl9SetAspectRatioMode, SetAspectRatioMode, SetAspectRatioMode method [DirectShow], SetAspectRatioMode method [DirectShow],IVMRWindowlessControl9 interface, dshow.ivmrwindowlesscontrol9_setaspectratiomode, vmr9/IVMRWindowlessControl9::SetAspectRatioMode
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
 - IVMRWindowlessControl9::SetAspectRatioMode
 - vmr9/IVMRWindowlessControl9::SetAspectRatioMode
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
 - IVMRWindowlessControl9.SetAspectRatioMode
---

# IVMRWindowlessControl9::SetAspectRatioMode


## -description

The <code>SetAspectRatioMode</code> method sets the current aspect ratio display mode.

## -parameters

### -param AspectRatioMode [in]

A <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9aspectratiomode">VMR9AspectRatioMode</a> value that specifies the aspect ratio mode.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
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

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getaspectratiomode">GetAspectRatioMode</a>



<a href="/previous-versions/ms787155(v=vs.85)">IVMRWindowlessControl9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>