---
UID: NF:strmif.IPinConnection.DynamicDisconnect
title: IPinConnection::DynamicDisconnect (strmif.h)
description: The DynamicDisconnect method disconnects the pin when the filter is active (paused or running). Call this method instead of IPin::Disconnect to disconnect a pin when the graph is running or paused.
helpviewer_keywords: ["DynamicDisconnect","DynamicDisconnect method [DirectShow]","DynamicDisconnect method [DirectShow]","IPinConnection interface","IPinConnection interface [DirectShow]","DynamicDisconnect method","IPinConnection.DynamicDisconnect","IPinConnection::DynamicDisconnect","IPinConnectionDynamicDisconnect","dshow.ipinconnection_dynamicdisconnect","strmif/IPinConnection::DynamicDisconnect"]
old-location: dshow\ipinconnection_dynamicdisconnect.htm
tech.root: dshow
ms.assetid: 44a5a219-fd42-4fe1-a767-f74d01d86012
ms.date: 12/05/2018
ms.keywords: DynamicDisconnect, DynamicDisconnect method [DirectShow], DynamicDisconnect method [DirectShow],IPinConnection interface, IPinConnection interface [DirectShow],DynamicDisconnect method, IPinConnection.DynamicDisconnect, IPinConnection::DynamicDisconnect, IPinConnectionDynamicDisconnect, dshow.ipinconnection_dynamicdisconnect, strmif/IPinConnection::DynamicDisconnect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPinConnection::DynamicDisconnect
 - strmif/IPinConnection::DynamicDisconnect
dev_langs:
 - c++
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
---

# IPinConnection::DynamicDisconnect


## -description

The <code>DynamicDisconnect</code> method disconnects the pin when the filter is active (paused or running). Call this method instead of <a href="/windows/desktop/api/strmif/nf-strmif-ipin-disconnect">IPin::Disconnect</a> to disconnect a pin when the graph is running or paused.



The caller must ensure that no data is flowing to the pin when it calls this method. Call the <a href="/windows/desktop/api/strmif/nf-strmif-ipinflowcontrol-block">IPinFlowControl::Block</a> method on an upstream pin to block the data flow, or use some other mechanism to make sure that no samples are delivered until this pin is reconnected.



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

<a href="/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>



<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection Interface</a>
