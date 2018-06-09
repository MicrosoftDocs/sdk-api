---
UID: NN:sbe.IStreamBufferConfigure3
title: IStreamBufferConfigure3
author: windows-sdk-content
description: The IStreamBufferConfigure3 interface is exposed by the StreamBufferConfig object.
old-location: mstv\istreambufferconfigure3.htm
old-project: mstv
ms.assetid: 73f3cd43-11d1-4eff-861d-087bfda7d135
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IStreamBufferConfigure3, IStreamBufferConfigure3 interface [Microsoft TV Technologies], IStreamBufferConfigure3 interface [Microsoft TV Technologies],described, IStreamBufferConfigure3Interface, mstv.istreambufferconfigure3, sbe/IStreamBufferConfigure3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure3
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStreamBufferConfigure3 interface


## -description



The <b>IStreamBufferConfigure3</b> interface is exposed by the <a href="https://msdn.microsoft.com/10678f33-2117-4add-8e4b-7b4d4eed11a9">StreamBufferConfig</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferConfigure3</b> interface inherits from <a href="https://msdn.microsoft.com/df71783c-1ff3-46b0-bae2-61d12f4d70d0">IStreamBufferConfigure2</a>. <b>IStreamBufferConfigure3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferConfigure3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c03b5edd-e2b2-4ac9-b2e7-080f3796a6cc">GetNamespace</a>
</td>
<td align="left" width="63%">
Retrieves the prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caf50c08-5247-4229-8952-9d538362b33d">GetStartRecConfig</a>
</td>
<td align="left" width="63%">
Queries whether the <a href="https://msdn.microsoft.com/e72ec34e-d3e3-4f5f-9336-d55135dc1e47">IStreamBufferRecordControl::Start</a> method automatically stops the current recording.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e009e078-99f5-4da1-88ce-c07e9588c5e8">SetNamespace</a>
</td>
<td align="left" width="63%">
Specifies a prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ae896ce-72e8-49aa-a538-2a269ef07ade">SetStartRecConfig</a>
</td>
<td align="left" width="63%">
Specifies whether the <b>IStreamBufferRecordControl::Start</b> method automatically stops the current recording.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferConfigure3)</code>.




## -see-also




<a href="https://msdn.microsoft.com/df71783c-1ff3-46b0-bae2-61d12f4d70d0">IStreamBufferConfigure2</a>



<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

