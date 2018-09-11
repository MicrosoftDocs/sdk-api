---
UID: NF:strmif.IPinConnection.DynamicDisconnect
title: IPinConnection::DynamicDisconnect
author: windows-sdk-content
description: The DynamicDisconnect method disconnects the pin when the filter is active (paused or running). Call this method instead of IPin::Disconnect to disconnect a pin when the graph is running or paused.
old-location: dshow\ipinconnection_dynamicdisconnect.htm
tech.root: DirectShow
ms.assetid: 44a5a219-fd42-4fe1-a767-f74d01d86012
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: DynamicDisconnect, DynamicDisconnect method [DirectShow], DynamicDisconnect method [DirectShow],IPinConnection interface, IPinConnection interface [DirectShow],DynamicDisconnect method, IPinConnection.DynamicDisconnect, IPinConnection::DynamicDisconnect, IPinConnectionDynamicDisconnect, dshow.ipinconnection_dynamicdisconnect, strmif/IPinConnection::DynamicDisconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IPinConnection.DynamicDisconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPinConnection::DynamicDisconnect


## -description



The <code>DynamicDisconnect</code> method disconnects the pin when the filter is active (paused or running). Call this method instead of <a href="https://msdn.microsoft.com/46e1e99c-848b-4936-b6bf-4ef1703a1f42">IPin::Disconnect</a> to disconnect a pin when the graph is running or paused.



The caller must ensure that no data is flowing to the pin when it calls this method. Call the <a href="https://msdn.microsoft.com/9bcd325d-41fc-4166-8fce-50fc921efdba">IPinFlowControl::Block</a> method on an upstream pin to block the data flow, or use some other mechanism to make sure that no samples are delivered until this pin is reconnected.


## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The pin is already disconnected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5b777f64-6b62-48dd-8eae-6603582a452a">Dynamic Reconnection</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection Interface</a>
 

 

