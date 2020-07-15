---
UID: NN:strmif.IPinConnection
title: IPinConnection (strmif.h)
description: This interface provides methods for reconnecting an input pin while the filter is still running.
helpviewer_keywords: ["IPinConnection","IPinConnection interface [DirectShow]","IPinConnection interface [DirectShow]","described","IPinConnectionInterface","dshow.ipinconnection","strmif/IPinConnection"]
old-location: dshow\ipinconnection.htm
tech.root: DirectShow
ms.assetid: 0843a01c-6f6a-4765-abca-dd562175fcee
ms.date: 12/05/2018
ms.keywords: IPinConnection, IPinConnection interface [DirectShow], IPinConnection interface [DirectShow],described, IPinConnectionInterface, dshow.ipinconnection, strmif/IPinConnection
f1_keywords:
- strmif/IPinConnection
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPinConnection interface


## -description



This interface provides methods for reconnecting an input pin while the filter is still running. The Filter Graph Manager calls methods on this interface when it performs dynamic reconnections (see the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphconfig">IGraphConfig</a> interface). Applications might also use this interface to perform dynamic pin reconnections.

<b>Filter developers: </b>Implement this interface on any input pin that allows dynamic reconnection or dynamic changes in format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPinConnection</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPinConnection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipinconnection-dynamicdisconnect">DynamicDisconnect</a>
</td>
<td align="left" width="63%">
Disconnects the pin when the filter is running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipinconnection-dynamicqueryaccept">DynamicQueryAccept</a>
</td>
<td align="left" width="63%">
Queries whether the pin can accept the specified media type while the graph is running with the current connection to this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipinconnection-isendpin">IsEndPin</a>
</td>
<td align="left" width="63%">
Indicates whether a reconnection search should end at this pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipinconnection-notifyendofstream">NotifyEndOfStream</a>
</td>
<td align="left" width="63%">
Requests notification from the pin when the next end-of-stream condition occurs.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dynamic-graph-building">Dynamic Graph Building</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>
 

 

