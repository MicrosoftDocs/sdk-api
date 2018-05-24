---
UID: NN:sbe.IStreamBufferSource
title: IStreamBufferSource
author: windows-driver-content
description: The IStreamBufferSource interface is exposed by the Stream Buffer Source filter. Use this interface to play live content from the Stream Buffer Sink filter.
old-location: mstv\istreambuffersource.htm
old-project: mstv
ms.assetid: 1e407f85-820a-4d17-926d-0c00e1e453e2
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IStreamBufferSource, IStreamBufferSource interface [Microsoft TV Technologies], IStreamBufferSource interface [Microsoft TV Technologies],described, IStreamBufferSourceInterface, mstv.istreambuffersource, sbe/IStreamBufferSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
-	IStreamBufferSource
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStreamBufferSource interface


## -description



The <b>IStreamBufferSource</b> interface is exposed by the <a href="https://msdn.microsoft.com/435081e9-8a3f-42ab-9091-30c7c3dd59c6">Stream Buffer Source</a> filter. Use this interface to play live content from the <a href="https://msdn.microsoft.com/e49fe3c2-e77f-419a-910c-78f72ebdfdbc">Stream Buffer Sink</a> filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cc53fb6-a652-43fa-a962-9bd3c67b5664">SetStreamSink</a>
</td>
<td align="left" width="63%">
Sets a pointer to the Stream Buffer Sink filter, so that the source filter can stream data from the sink filter.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferSource)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>



<a href="https://msdn.microsoft.com/aa19d268-fbeb-4dc4-a8f5-8bc31a85367f">Using the Stream Buffer Engine</a>
 

 

