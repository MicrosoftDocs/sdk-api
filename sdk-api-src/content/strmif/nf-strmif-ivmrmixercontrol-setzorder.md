---
UID: NF:strmif.IVMRMixerControl.SetZOrder
title: IVMRMixerControl::SetZOrder (strmif.h)
description: The SetZOrder method sets this video stream's position in the Z-order; larger values are further away.helpviewer_keywords: ["IVMRMixerControl interface [DirectShow]","SetZOrder method","IVMRMixerControl.SetZOrder","IVMRMixerControl::SetZOrder","IVMRMixerControlSetZOrder","SetZOrder","SetZOrder method [DirectShow]","SetZOrder method [DirectShow]","IVMRMixerControl interface","dshow.ivmrmixercontrol_setzorder","strmif/IVMRMixerControl::SetZOrder"]
old-location: dshow\ivmrmixercontrol_setzorder.htm
tech.root: DirectShow
ms.assetid: f1ef562e-049c-4edf-a83c-76675e2113c6
ms.date: 12/05/2018
ms.keywords: IVMRMixerControl interface [DirectShow],SetZOrder method, IVMRMixerControl.SetZOrder, IVMRMixerControl::SetZOrder, IVMRMixerControlSetZOrder, SetZOrder, SetZOrder method [DirectShow], SetZOrder method [DirectShow],IVMRMixerControl interface, dshow.ivmrmixercontrol_setzorder, strmif/IVMRMixerControl::SetZOrder
f1_keywords:
- strmif/IVMRMixerControl.SetZOrder
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
- IVMRMixerControl.SetZOrder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerControl::SetZOrder


## -description



The <code>SetZOrder</code> method sets this video stream's position in the Z-order; larger values are further away.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param dwZ [in]

Double word containing the stream's position within the Z-order.


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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected.

</td>
</tr>
</table>
 




## -remarks



The default Z-order is the order in which the pins were created. You only need to use this method if you wish to modify the default Z-order.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-getzorder">IVMRMixerControl::GetZOrder</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

