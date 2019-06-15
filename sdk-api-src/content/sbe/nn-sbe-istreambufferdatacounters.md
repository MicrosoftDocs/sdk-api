---
UID: NN:sbe.IStreamBufferDataCounters
title: IStreamBufferDataCounters (sbe.h)
author: windows-sdk-content
description: The IStreamBufferDataCounters interface returns performance statistics for the Stream Buffer filters. This interface is exposed by the pins on the Stream Buffer Sink filter and the Stream Buffer Source filter.
old-location: mstv\istreambufferdatacounters.htm
tech.root: mstv
ms.assetid: d9394d04-ba6b-4946-b33a-9c53070238f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStreamBufferDataCounters, IStreamBufferDataCounters interface [Microsoft TV Technologies], IStreamBufferDataCounters interface [Microsoft TV Technologies],described, IStreamBufferDataCountersInterface, mstv.istreambufferdatacounters, sbe/IStreamBufferDataCounters
ms.topic: interface
f1_keywords: ["sbe/IStreamBufferDataCounters"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferDataCounters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferDataCounters interface


## -description



The <b>IStreamBufferDataCounters</b> interface returns performance statistics for the Stream Buffer filters. This interface is exposed by the pins on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter and the Stream Buffer Source filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferDataCounters</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferDataCounters</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferdatacounters-getdata">GetData</a>
</td>
<td align="left" width="63%">
Returns performance data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferdatacounters-resetdata">ResetData</a>
</td>
<td align="left" width="63%">
Resets the performance counters.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferDataCounters)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

