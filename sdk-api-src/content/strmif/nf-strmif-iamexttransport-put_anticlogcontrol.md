---
UID: NF:strmif.IAMExtTransport.put_AntiClogControl
title: IAMExtTransport::put_AntiClogControl
author: windows-driver-content
description: The put_AntiClogControl method enables or disables anti-headclog control on the transport.
old-location: dshow\iamexttransport_put_anticlogcontrol.htm
old-project: DirectShow
ms.assetid: 02d1e400-9959-4c68-ad8e-bc1700205179
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMExtTransport interface [DirectShow],put_AntiClogControl method, IAMExtTransport.put_AntiClogControl, IAMExtTransport::put_AntiClogControl, IAMExtTransportput_AntiClogControl, dshow.iamexttransport_put_anticlogcontrol, put_AntiClogControl, put_AntiClogControl method [DirectShow], put_AntiClogControl method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_AntiClogControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMExtTransport.put_AntiClogControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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
<th>
                  Value
                </th>
<th>
                  Description
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

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/e0175b44-d1e6-4f3a-8aa7-893b41d0c487">IAMExtTransport::get_AntiClogControl</a>
 

 

