---
UID: NF:strmif.IVMRWindowlessControl.SetColorKey
title: IVMRWindowlessControl::SetColorKey (strmif.h)
description: The SetColorKey method sets the source color key value that the VMR should use.
helpviewer_keywords: ["IVMRWindowlessControl interface [DirectShow]","SetColorKey method","IVMRWindowlessControl.SetColorKey","IVMRWindowlessControl::SetColorKey","IVMRWindowlessControlSetColorKey","SetColorKey","SetColorKey method [DirectShow]","SetColorKey method [DirectShow]","IVMRWindowlessControl interface","dshow.ivmrwindowlesscontrol_setcolorkey","strmif/IVMRWindowlessControl::SetColorKey"]
old-location: dshow\ivmrwindowlesscontrol_setcolorkey.htm
tech.root: dshow
ms.assetid: 9facf4af-ed56-4a94-b351-35ddd7f63e6e
ms.date: 12/05/2018
ms.keywords: IVMRWindowlessControl interface [DirectShow],SetColorKey method, IVMRWindowlessControl.SetColorKey, IVMRWindowlessControl::SetColorKey, IVMRWindowlessControlSetColorKey, SetColorKey, SetColorKey method [DirectShow], SetColorKey method [DirectShow],IVMRWindowlessControl interface, dshow.ivmrwindowlesscontrol_setcolorkey, strmif/IVMRWindowlessControl::SetColorKey
f1_keywords:
- strmif/IVMRWindowlessControl.SetColorKey
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IVMRWindowlessControl.SetColorKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRWindowlessControl::SetColorKey


## -description



The <code>SetColorKey</code> method sets the source color key value that the VMR should use.




## -parameters




### -param Clr [in]

Specifies the source color key.


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
 




## -remarks



Color key control is only meaningful when the VMR is using an overlay surface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrwindowlesscontrol">IVMRWindowlessControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-getcolorkey">IVMRWindowlessControl::GetColorKey</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

