---
UID: NF:windows.media.streaming.IBasicDevice.remove_ConnectionStatusChanged
title: IBasicDevice::streaming
author: windows-sdk-content
description: Unregisters an event handler for the ConnectionStatusChanged event.
old-location: mediastreaming\ibasicdevice_remove_connectionstatuschanged.htm
tech.root: mediastreaming
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBasicDevice interface [Media Streaming API],remove_ConnectionStatusChanged method, IBasicDevice.remove_ConnectionStatusChanged, IBasicDevice.streaming, IBasicDevice::remove_ConnectionStatusChanged, IBasicDevice::streaming, mediastreaming.ibasicdevice_remove_connectionstatuschanged, remove_ConnectionStatusChanged, remove_ConnectionStatusChanged method [Media Streaming API], remove_ConnectionStatusChanged method [Media Streaming API],IBasicDevice interface, windows/IBasicDevice::remove_ConnectionStatusChanged
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
 - IBasicDevice.remove_ConnectionStatusChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBasicDevice::streaming


## -description


Unregisters an event handler for the <a href="https://msdn.microsoft.com/D1F04FA5-895E-4E86-9643-E880388DCDED">ConnectionStatusChanged</a> event.


## -parameters




### -param token [in]

A reference to a token obtained from the <a href="https://msdn.microsoft.com/1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399">add_ConnectionStatusChanged</a> method when the event handler was registered.


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
 




## -see-also




<a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>
 

 

