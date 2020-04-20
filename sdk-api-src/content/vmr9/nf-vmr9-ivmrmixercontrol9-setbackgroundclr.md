---
UID: NF:vmr9.IVMRMixerControl9.SetBackgroundClr
title: IVMRMixerControl9::SetBackgroundClr (vmr9.h)
description: The SetBackgroundClr method sets the background color on the output rectangle.helpviewer_keywords: ["IVMRMixerControl9 interface [DirectShow]","SetBackgroundClr method","IVMRMixerControl9.SetBackgroundClr","IVMRMixerControl9::SetBackgroundClr","IVMRMixerControl9SetBackgroundClr","SetBackgroundClr","SetBackgroundClr method [DirectShow]","SetBackgroundClr method [DirectShow]","IVMRMixerControl9 interface","dshow.ivmrmixercontrol9_setbackgroundclr","vmr9/IVMRMixerControl9::SetBackgroundClr"]
old-location: dshow\ivmrmixercontrol9_setbackgroundclr.htm
tech.root: DirectShow
ms.assetid: fed7f4bb-519c-4e02-be99-065b9131e57c
ms.date: 12/05/2018
ms.keywords: IVMRMixerControl9 interface [DirectShow],SetBackgroundClr method, IVMRMixerControl9.SetBackgroundClr, IVMRMixerControl9::SetBackgroundClr, IVMRMixerControl9SetBackgroundClr, SetBackgroundClr, SetBackgroundClr method [DirectShow], SetBackgroundClr method [DirectShow],IVMRMixerControl9 interface, dshow.ivmrmixercontrol9_setbackgroundclr, vmr9/IVMRMixerControl9::SetBackgroundClr
f1_keywords:
- vmr9/IVMRMixerControl9.SetBackgroundClr
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRMixerControl9.SetBackgroundClr
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerControl9::SetBackgroundClr


## -description



The <code>SetBackgroundClr</code> method sets the background color on the output rectangle.




## -parameters




### -param ClrBkg [in]

Specifies the background color.


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




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrmixercontrol9">IVMRMixerControl9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

