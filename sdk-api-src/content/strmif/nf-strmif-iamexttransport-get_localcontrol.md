---
UID: NF:strmif.IAMExtTransport.get_LocalControl
title: IAMExtTransport::get_LocalControl (strmif.h)
author: windows-sdk-content
description: The get_LocalControl method determines whether the transport is under local control or remote control.
old-location: dshow\iamexttransport_get_localcontrol.htm
tech.root: DirectShow
ms.assetid: 793078a2-bddd-469b-9043-f07830499353
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMExtTransport interface [DirectShow],get_LocalControl method, IAMExtTransport.get_LocalControl, IAMExtTransport::get_LocalControl, IAMExtTransportget_LocalControl, dshow.iamexttransport_get_localcontrol, get_LocalControl, get_LocalControl method [DirectShow], get_LocalControl method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_LocalControl
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
 - IAMExtTransport.get_LocalControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMExtTransport::get_LocalControl


## -description



The <code>get_LocalControl</code> method determines whether the transport is under local control or remote control.



This method is not implemented.


## -parameters




### -param pState [out]

Pointer to a <b>long</b> integer that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Local control.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Remote control.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



To control an external device from an application, the device must be in remote mode.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://docs.microsoft.com/windows/desktop/DirectShow/msdv-driver">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamexttransport-put_localcontrol">IAMExtTransport::put_LocalControl</a>
 

 

