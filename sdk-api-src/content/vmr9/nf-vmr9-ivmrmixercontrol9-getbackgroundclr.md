---
UID: NF:vmr9.IVMRMixerControl9.GetBackgroundClr
title: IVMRMixerControl9::GetBackgroundClr (vmr9.h)
description: The GetBackgroundClr method gets the current background color on the output rectangle.
helpviewer_keywords: ["GetBackgroundClr","GetBackgroundClr method [DirectShow]","GetBackgroundClr method [DirectShow]","IVMRMixerControl9 interface","IVMRMixerControl9 interface [DirectShow]","GetBackgroundClr method","IVMRMixerControl9.GetBackgroundClr","IVMRMixerControl9::GetBackgroundClr","IVMRMixerControl9GetBackgroundClr","dshow.ivmrmixercontrol9_getbackgroundclr","vmr9/IVMRMixerControl9::GetBackgroundClr"]
old-location: dshow\ivmrmixercontrol9_getbackgroundclr.htm
tech.root: dshow
ms.assetid: 1be2fb34-b0f3-4dff-8813-a487229af6dc
ms.date: 12/05/2018
ms.keywords: GetBackgroundClr, GetBackgroundClr method [DirectShow], GetBackgroundClr method [DirectShow],IVMRMixerControl9 interface, IVMRMixerControl9 interface [DirectShow],GetBackgroundClr method, IVMRMixerControl9.GetBackgroundClr, IVMRMixerControl9::GetBackgroundClr, IVMRMixerControl9GetBackgroundClr, dshow.ivmrmixercontrol9_getbackgroundclr, vmr9/IVMRMixerControl9::GetBackgroundClr
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
 - IVMRMixerControl9::GetBackgroundClr
 - vmr9/IVMRMixerControl9::GetBackgroundClr
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
 - IVMRMixerControl9.GetBackgroundClr
---

# IVMRMixerControl9::GetBackgroundClr


## -description

The <code>GetBackgroundClr</code> method gets the current background color on the output rectangle.

## -parameters

### -param lpClrBkg [in]

Pointer to a variable that receives the background color.

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
</table>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmixercontrol9-setbackgroundclr">SetBackgroundClr</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>