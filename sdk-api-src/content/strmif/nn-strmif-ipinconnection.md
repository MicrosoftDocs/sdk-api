---
UID: NN:strmif.IPinConnection
title: IPinConnection
author: windows-sdk-content
description: This interface provides methods for reconnecting an input pin while the filter is still running.
old-location: dshow\ipinconnection.htm
tech.root: DirectShow
ms.assetid: 0843a01c-6f6a-4765-abca-dd562175fcee
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IPinConnection, IPinConnection interface [DirectShow], IPinConnection interface [DirectShow],described, IPinConnectionInterface, dshow.ipinconnection, strmif/IPinConnection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IPinConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPinConnection interface


## -description



This interface provides methods for reconnecting an input pin while the filter is still running. The Filter Graph Manager calls methods on this interface when it performs dynamic reconnections (see the <a href="https://msdn.microsoft.com/7df22157-9dd1-410e-b037-a155f7b9a01b">IGraphConfig</a> interface). Applications might also use this interface to perform dynamic pin reconnections.

<b>Filter developers: </b>Implement this interface on any input pin that allows dynamic reconnection or dynamic changes in format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPinConnection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPinConnection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPinConnection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44a5a219-fd42-4fe1-a767-f74d01d86012">DynamicDisconnect</a>
</td>
<td align="left" width="63%">
Disconnects the pin when the filter is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86a4f18c-4bd0-45d2-bb5a-b0f41cd0ab43">DynamicQueryAccept</a>
</td>
<td align="left" width="63%">
Queries whether the pin can accept the specified media type while the graph is running with the current connection to this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e078c952-2c3b-48cd-a898-ac2de9fc359a">IsEndPin</a>
</td>
<td align="left" width="63%">
Indicates whether a reconnection search should end at this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a911436-a679-4a86-93f9-e9c57ca762c5">NotifyEndOfStream</a>
</td>
<td align="left" width="63%">
Requests notification from the pin when the next end-of-stream condition occurs.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/13fed430-979b-40f7-91ba-aff2d811bd92">Dynamic Graph Building</a>



<a href="https://msdn.microsoft.com/5b777f64-6b62-48dd-8eae-6603582a452a">Dynamic Reconnection</a>
 

 

