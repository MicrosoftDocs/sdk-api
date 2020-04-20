---
UID: NF:vmr9.IVMRFilterConfig9.SetRenderingMode
title: IVMRFilterConfig9::SetRenderingMode (vmr9.h)
description: The SetRenderingMode method sets the rendering mode used by the VMR.helpviewer_keywords: ["IVMRFilterConfig9 interface [DirectShow]","SetRenderingMode method","IVMRFilterConfig9.SetRenderingMode","IVMRFilterConfig9::SetRenderingMode","IVMRFilterConfig9SetRenderingMode","SetRenderingMode","SetRenderingMode method [DirectShow]","SetRenderingMode method [DirectShow]","IVMRFilterConfig9 interface","dshow.ivmrfilterconfig9_setrenderingmode","vmr9/IVMRFilterConfig9::SetRenderingMode"]
old-location: dshow\ivmrfilterconfig9_setrenderingmode.htm
tech.root: DirectShow
ms.assetid: d7a27d7c-5cd4-4a20-ba15-7056d502e3e3
ms.date: 12/05/2018
ms.keywords: IVMRFilterConfig9 interface [DirectShow],SetRenderingMode method, IVMRFilterConfig9.SetRenderingMode, IVMRFilterConfig9::SetRenderingMode, IVMRFilterConfig9SetRenderingMode, SetRenderingMode, SetRenderingMode method [DirectShow], SetRenderingMode method [DirectShow],IVMRFilterConfig9 interface, dshow.ivmrfilterconfig9_setrenderingmode, vmr9/IVMRFilterConfig9::SetRenderingMode
f1_keywords:
- vmr9/IVMRFilterConfig9.SetRenderingMode
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
- IVMRFilterConfig9.SetRenderingMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRFilterConfig9::SetRenderingMode


## -description



The <code>SetRenderingMode</code> method sets the rendering mode used by the VMR.




## -parameters




### -param Mode [in]

Specifies the rendering mode as a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9mode">VMR9Mode</a> value.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid rendering mode was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
The mode cannot be changed for some reason. See Remarks.

</td>
</tr>
</table>
 




## -remarks



The VMR is in windowed mode (<b>VMR9Mode_Windowed</b>) by default. Use this method to put the VMR into windowless mode (<b>VMR9Mode_Windowless</b>) or renderless mode (<b>VMR9Mode_Renderless</b>).

The mode cannot be changed after any pin has been connected. Also, the mode cannot be changed from windowless or renderless mode back to windowed mode, even before pins are connected. Therefore, specifying <b>VMR9Mode_Windowed</b> for the <i>Mode</i> parameter has no effect under any circumstances.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrfilterconfig9">IVMRFilterConfig9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/vmr-modes-of-operation">VMR Modes of Operation</a>
 

 

