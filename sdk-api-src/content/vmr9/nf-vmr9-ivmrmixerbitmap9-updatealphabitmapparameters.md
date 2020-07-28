---
UID: NF:vmr9.IVMRMixerBitmap9.UpdateAlphaBitmapParameters
title: IVMRMixerBitmap9::UpdateAlphaBitmapParameters (vmr9.h)
description: The UpdateAlphaBitmapParameters method changes the bitmap location, size and blending value.
helpviewer_keywords: ["IVMRMixerBitmap9 interface [DirectShow]","UpdateAlphaBitmapParameters method","IVMRMixerBitmap9.UpdateAlphaBitmapParameters","IVMRMixerBitmap9::UpdateAlphaBitmapParameters","IVMRMixerBitmap9UpdateAlphaBitmapParameters","UpdateAlphaBitmapParameters","UpdateAlphaBitmapParameters method [DirectShow]","UpdateAlphaBitmapParameters method [DirectShow]","IVMRMixerBitmap9 interface","dshow.ivmrmixerbitmap9_updatealphabitmapparameters","vmr9/IVMRMixerBitmap9::UpdateAlphaBitmapParameters"]
old-location: dshow\ivmrmixerbitmap9_updatealphabitmapparameters.htm
tech.root: dshow
ms.assetid: 89aa0212-9311-4f23-9f55-7e7a1072a19a
ms.date: 12/05/2018
ms.keywords: IVMRMixerBitmap9 interface [DirectShow],UpdateAlphaBitmapParameters method, IVMRMixerBitmap9.UpdateAlphaBitmapParameters, IVMRMixerBitmap9::UpdateAlphaBitmapParameters, IVMRMixerBitmap9UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters, UpdateAlphaBitmapParameters method [DirectShow], UpdateAlphaBitmapParameters method [DirectShow],IVMRMixerBitmap9 interface, dshow.ivmrmixerbitmap9_updatealphabitmapparameters, vmr9/IVMRMixerBitmap9::UpdateAlphaBitmapParameters
f1_keywords:
- vmr9/IVMRMixerBitmap9.UpdateAlphaBitmapParameters
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
- IVMRMixerBitmap9.UpdateAlphaBitmapParameters
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerBitmap9::UpdateAlphaBitmapParameters


## -description



The <code>UpdateAlphaBitmapParameters</code> method changes the bitmap location, size and blending value.




## -parameters




### -param pBmpParms [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9alphabitmap">VMR9AlphaBitmap</a> structure.


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



The filter graph must be running for the changes to take effect. This method does not change the bitmap image. If you specify a <b>VMR9AlphaBitmap</b> structure with no destination or color key set, the bitmap is not displayed. This behavior was implemented for backward compatibility.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrmixerbitmap9">IVMRMixerBitmap9 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

