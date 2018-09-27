---
UID: NN:strmif.IPinFlowControl
title: IPinFlowControl
author: windows-sdk-content
description: Blocks data flow from an active output pin.
old-location: dshow\ipinflowcontrol.htm
tech.root: DirectShow
ms.assetid: 27e607d9-85f0-4e17-b8e7-6df729288acd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPinFlowControl, IPinFlowControl interface [DirectShow], IPinFlowControl interface [DirectShow],described, IPinFlowControlInterface, dshow.ipinflowcontrol, strmif/IPinFlowControl
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
 - IPinFlowControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPinFlowControl interface


## -description



Blocks data flow from an active output pin. This interface is exposed by output pins that can reconnect dynamically. Use this interface to start a dynamic reconnection within the filter graph. For more information, see <a href="https://msdn.microsoft.com/13fed430-979b-40f7-91ba-aff2d811bd92">Dynamic Graph Building</a>.

<b>Filter developers: </b>Parser and capture filters that support dynamic reconnection should support this interface on their output pins. Generally, other types of filters do not need to implement this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPinFlowControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPinFlowControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPinFlowControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bcd325d-41fc-4166-8fce-50fc921efdba">Block</a>
</td>
<td align="left" width="63%">
Blocks or unblocks the flow of data from the pin.

</td>
</tr>
</table> 

