---
UID: NF:strmif.IVMRMixerControl.GetZOrder
title: IVMRMixerControl::GetZOrder (strmif.h)
description: The GetZOrder method retrieves this video stream's position in the Z order.helpviewer_keywords: ["GetZOrder","GetZOrder method [DirectShow]","GetZOrder method [DirectShow]","IVMRMixerControl interface","IVMRMixerControl interface [DirectShow]","GetZOrder method","IVMRMixerControl.GetZOrder","IVMRMixerControl::GetZOrder","IVMRMixerControlGetZOrder","dshow.ivmrmixercontrol_getzorder","strmif/IVMRMixerControl::GetZOrder"]
old-location: dshow\ivmrmixercontrol_getzorder.htm
tech.root: DirectShow
ms.assetid: 76f84c77-e528-4059-8f40-5e49db9ec567
ms.date: 12/05/2018
ms.keywords: GetZOrder, GetZOrder method [DirectShow], GetZOrder method [DirectShow],IVMRMixerControl interface, IVMRMixerControl interface [DirectShow],GetZOrder method, IVMRMixerControl.GetZOrder, IVMRMixerControl::GetZOrder, IVMRMixerControlGetZOrder, dshow.ivmrmixercontrol_getzorder, strmif/IVMRMixerControl::GetZOrder
f1_keywords:
- strmif/IVMRMixerControl.GetZOrder
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
- IVMRMixerControl.GetZOrder
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRMixerControl::GetZOrder


## -description



The <code>GetZOrder</code> method retrieves this video stream's position in the Z order.




## -parameters




### -param dwStreamID [in]

Specifies the input stream.


### -param pZ [out]

Pointer to a DWORD that receives the current position in the Z-order.


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
<i>pZOrder</i> is invalid.

</td>
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



The default Z-order is the order in which the pins were created.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrmixercontrol">IVMRMixerControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrmixercontrol-setzorder">IVMRMixerControl::SetZOrder</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

