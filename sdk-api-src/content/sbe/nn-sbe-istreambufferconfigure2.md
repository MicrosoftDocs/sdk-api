---
UID: NN:sbe.IStreamBufferConfigure2
title: IStreamBufferConfigure2
author: windows-sdk-content
description: The IStreamBufferConfigure2 interface is exposed by the StreamBufferConfig object.
old-location: mstv\istreambufferconfigure2.htm
old-project: mstv
ms.assetid: df71783c-1ff3-46b0-bae2-61d12f4d70d0
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IStreamBufferConfigure2, IStreamBufferConfigure2 interface [Microsoft TV Technologies], IStreamBufferConfigure2 interface [Microsoft TV Technologies],described, IStreamBufferConfigure2Interface, mstv.istreambufferconfigure2, sbe/IStreamBufferConfigure2
ms.prod: windows
ms.technology: windows-sdk
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
 - IStreamBufferConfigure2
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: ADAM
---

# IStreamBufferConfigure2 interface


## -description



The <b>IStreamBufferConfigure2</b> interface is exposed by the <a href="https://msdn.microsoft.com/10678f33-2117-4add-8e4b-7b4d4eed11a9">StreamBufferConfig</a> object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferConfigure2</b> interface inherits from <a href="https://msdn.microsoft.com/8874fefd-2241-4b04-a7d5-191e13743fa0">IStreamBufferConfigure</a>. <b>IStreamBufferConfigure2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferConfigure2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba0ce9b2-f160-4749-92ba-b9a77f34b980">GetFFTransitionRates</a>
</td>
<td align="left" width="63%">
Returns the maximum full-frame and key-frame playback rates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36b5cd06-ba6a-4546-98b6-4c8b47f7f62b">GetMultiplexedPacketSize</a>
</td>
<td align="left" width="63%">
Returns the size of the multiplexed packets in the backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6e7b27a-b217-4430-adf7-c7ebc7e17bf6">SetFFTransitionRates</a>
</td>
<td align="left" width="63%">
Sets the behavior of fast-forward play ("trick mode").

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9133331b-cf0c-4dfb-8bb6-101742d194c7">SetMultiplexedPacketSize</a>
</td>
<td align="left" width="63%">
Sets the size of the multiplexed packets in the backing files.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferConfigure2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/8874fefd-2241-4b04-a7d5-191e13743fa0">IStreamBufferConfigure</a>



<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

