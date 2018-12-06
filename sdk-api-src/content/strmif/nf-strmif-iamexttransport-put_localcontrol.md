---
UID: NF:strmif.IAMExtTransport.put_LocalControl
title: IAMExtTransport::put_LocalControl
author: windows-sdk-content
description: The put_LocalControl method switches the device between local and remote control.
old-location: dshow\iamexttransport_put_localcontrol.htm
tech.root: DirectShow
ms.assetid: 1ac75eb7-4b4c-402b-8e4e-f94488eccec1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMExtTransport interface [DirectShow],put_LocalControl method, IAMExtTransport.put_LocalControl, IAMExtTransport::put_LocalControl, IAMExtTransportput_LocalControl, dshow.iamexttransport_put_localcontrol, put_LocalControl, put_LocalControl method [DirectShow], put_LocalControl method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_LocalControl
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
 - IAMExtTransport.put_LocalControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMExtTransport::put_LocalControl


## -description



The <code>put_LocalControl</code> method switches the device between local and remote control.



This method is not implemented.


## -parameters




### -param State [in]

Specifies the state of the device.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Local control</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Remote control</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/793078a2-bddd-469b-9043-f07830499353">IAMExtTransport::get_LocalControl</a>
 

 

