---
UID: NF:strmif.IAMExtTransport.get_AntiClogControl
title: IAMExtTransport::get_AntiClogControl method
author: windows-driver-content
description: The get_AntiClogControl method determines whether the anti-headclog control is enabled or disabled.
old-location: dshow\iamexttransport_get_anticlogcontrol.htm
old-project: DirectShow
ms.assetid: e0175b44-d1e6-4f3a-8aa7-893b41d0c487
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMExtTransport, IAMExtTransport interface [DirectShow], get_AntiClogControl method, IAMExtTransport::get_AntiClogControl, IAMExtTransportget_AntiClogControl, dshow.iamexttransport_get_anticlogcontrol, get_AntiClogControl method [DirectShow], get_AntiClogControl method [DirectShow], IAMExtTransport interface, get_AntiClogControl,IAMExtTransport.get_AntiClogControl, strmif/IAMExtTransport::get_AntiClogControl
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
-	IAMExtTransport.get_AntiClogControl
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::get_AntiClogControl method


## -description



The <code>get_AntiClogControl</code> method determines whether the anti-headclog control is enabled or disabled.



This method is not implemented.


## -parameters




### -param pEnabled [out]

Pointer to a <b>long</b> integer that receives one of the following values:

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
<td>Anti-headclog is enabled.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Anti-headclog is disabled.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/02d1e400-9959-4c68-ad8e-bc1700205179">IAMExtTransport::put_AntiClogControl</a>
 

 

