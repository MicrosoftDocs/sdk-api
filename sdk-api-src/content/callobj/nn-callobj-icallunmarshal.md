---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ICallUnmarshal interface


## -description


Is used on the server (receiving) side of a remote invocation. An appropriate instance of <b>ICallUnmarshal</b> can be used to transform back into an call frame a method invocation previously marshaled by a call to <a href="https://msdn.microsoft.com/cab40c31-1f89-4da9-a1e0-ef946b34665c">ICallFrame::Marshal</a> on the client (sending) side. After such a reconstituted call frame is obtained, the call can be carried out on an actual object using <a href="https://msdn.microsoft.com/75cb7b96-55c9-4aee-b507-a549e2af38bc">ICallFrame::Invoke</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallUnmarshal</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>ICallUnmarshal</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICallUnmarshal</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7b1aff8-338a-491a-908f-5f85dddd89b7">ReleaseMarshalData</a>
</td>
<td align="left" width="63%">
Releases resources that may be held by interface pointers residing in a packet of marshaled data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15d04287-285d-43d9-ad55-3dc9c7ae192e">Unmarshal</a>
</td>
<td align="left" width="63%">
Turns a marshaled packet of data back into an activation record that can then be invoked or manipulated in some other way.

</td>
</tr>
</table> 

