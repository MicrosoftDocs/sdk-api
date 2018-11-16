---
UID: NF:windows.media.streaming.IBasicDevice.add_ConnectionStatusChanged
title: IBasicDevice::streaming
author: windows-sdk-content
description: Registers an event handler for the ConnectionStatusChanged event.
old-location: mediastreaming\ibasicdevice_add_connectionstatuschanged.htm
tech.root: mediastreaming
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBasicDevice interface [Media Streaming API],add_ConnectionStatusChanged method, IBasicDevice.add_ConnectionStatusChanged, IBasicDevice.streaming, IBasicDevice::add_ConnectionStatusChanged, IBasicDevice::streaming, add_ConnectionStatusChanged, add_ConnectionStatusChanged method [Media Streaming API], add_ConnectionStatusChanged method [Media Streaming API],IBasicDevice interface, mediastreaming.ibasicdevice_add_connectionstatuschanged, windows/IBasicDevice::add_ConnectionStatusChanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.streaming.h
api_name:
 - IBasicDevice.add_ConnectionStatusChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.media.streaming.h
: 
- IBasicDevice.add_ConnectionStatusChanged
: 
---

# IBasicDevice::streaming


## -description


Registers an event handler for the <a href="https://msdn.microsoft.com/D1F04FA5-895E-4E86-9643-E880388DCDED">ConnectionStatusChanged</a> event.


## -parameters




### -param handler [in]

A <a href="https://msdn.microsoft.com/ca659186-ae24-4823-b799-c96c84c5cfc1">ConnectionStatusHandler</a> event handler function.


### -param token [out, retval]

Reference to a token that can be used to unregister the event handler.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



To unregister the event handler that was registered by this method, pass the <i>token</i> value to the <a href="https://msdn.microsoft.com/577D9C50-486D-441A-A9FE-AF79D1FC2B52">remove_ConnectionStatusChanged</a> method.




## -see-also




<a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>
 

 

