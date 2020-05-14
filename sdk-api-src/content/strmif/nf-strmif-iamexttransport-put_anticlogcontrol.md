---
UID: NF:strmif.IAMExtTransport.put_AntiClogControl
title: IAMExtTransport::put_AntiClogControl (strmif.h)
description: The put_AntiClogControl method enables or disables anti-headclog control on the transport.helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","put_AntiClogControl method","IAMExtTransport.put_AntiClogControl","IAMExtTransport::put_AntiClogControl","IAMExtTransportput_AntiClogControl","dshow.iamexttransport_put_anticlogcontrol","put_AntiClogControl","put_AntiClogControl method [DirectShow]","put_AntiClogControl method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::put_AntiClogControl"]
old-location: dshow\iamexttransport_put_anticlogcontrol.htm
tech.root: DirectShow
ms.assetid: 02d1e400-9959-4c68-ad8e-bc1700205179
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],put_AntiClogControl method, IAMExtTransport.put_AntiClogControl, IAMExtTransport::put_AntiClogControl, IAMExtTransportput_AntiClogControl, dshow.iamexttransport_put_anticlogcontrol, put_AntiClogControl, put_AntiClogControl method [DirectShow], put_AntiClogControl method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_AntiClogControl
f1_keywords:
- strmif/IAMExtTransport.put_AntiClogControl
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- IAMExtTransport.put_AntiClogControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtTransport::put_AntiClogControl


## -description



The <code>put_AntiClogControl</code> method enables or disables anti-headclog control on the transport.



This method is not implemented.


## -parameters




### -param Enable [in]

Specifies whether to enable anti-headclog control.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Enable transport anti-headclog control.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Disable transport anti-headclog control.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



Use this method to unclog video heads on VCRs that have an automatic head-cleaning feature.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://docs.microsoft.com/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_anticlogcontrol">IAMExtTransport::get_AntiClogControl</a>
 

 

