---
UID: NN:sbe.IStreamBufferDataCounters
title: IStreamBufferDataCounters
author: windows-driver-content
description: The IStreamBufferDataCounters interface returns performance statistics for the Stream Buffer filters. This interface is exposed by the pins on the Stream Buffer Sink filter and the Stream Buffer Source filter.
old-location: mstv\istreambufferdatacounters.htm
old-project: mstv
ms.assetid: d9394d04-ba6b-4946-b33a-9c53070238f7
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IStreamBufferDataCounters, IStreamBufferDataCounters interface [Microsoft TV Technologies], IStreamBufferDataCounters interface [Microsoft TV Technologies],described, IStreamBufferDataCountersInterface, mstv.istreambufferdatacounters, sbe/IStreamBufferDataCounters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferDataCounters
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStreamBufferDataCounters interface


## -description



The <b>IStreamBufferDataCounters</b> interface returns performance statistics for the Stream Buffer filters. This interface is exposed by the pins on the <a href="https://msdn.microsoft.com/e49fe3c2-e77f-419a-910c-78f72ebdfdbc">Stream Buffer Sink</a> filter and the Stream Buffer Source filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferDataCounters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferDataCounters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferDataCounters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
</td>
<td align="left" width="63%">
Returns performance data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/643f0f67-8915-4097-b53a-7007610c9c8a">ResetData</a>
</td>
<td align="left" width="63%">
Resets the performance counters.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferDataCounters)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

