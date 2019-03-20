---
UID: NF:strmif.IAMExtTransport.get_LocalControl
title: IAMExtTransport::get_LocalControl (strmif.h)
author: windows-sdk-content
description: The get_LocalControl method determines whether the transport is under local control or remote control.
old-location: dshow\iamexttransport_get_localcontrol.htm
tech.root: DirectShow
ms.assetid: 793078a2-bddd-469b-9043-f07830499353
ms.author: windowssdkdev
ms.date: 12/5/2018
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

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/1ac75eb7-4b4c-402b-8e4e-f94488eccec1">IAMExtTransport::put_LocalControl</a>
 

 

