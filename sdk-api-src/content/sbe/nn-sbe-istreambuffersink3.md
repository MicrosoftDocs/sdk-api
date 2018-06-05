---
UID: NN:sbe.IStreamBufferSink3
title: IStreamBufferSink3
author: windows-sdk-content
description: The IStreamBufferSink3 interface is exposed by the Stream Buffer Sink filter.
old-location: mstv\istreambuffersink3.htm
old-project: mstv
ms.assetid: a3adbe79-7d7c-4b12-a574-23c64d2311af
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IStreamBufferSink3, IStreamBufferSink3 interface [Microsoft TV Technologies], IStreamBufferSink3 interface [Microsoft TV Technologies],described, IStreamBufferSink3Interface, mstv.istreambuffersink3, sbe/IStreamBufferSink3
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferSink3
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStreamBufferSink3 interface


## -description



The <b>IStreamBufferSink3</b> interface is exposed by the <a href="https://msdn.microsoft.com/e49fe3c2-e77f-419a-910c-78f72ebdfdbc">Stream Buffer Sink</a> filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferSink3</b> interface inherits from <a href="https://msdn.microsoft.com/ae97e1e2-011d-4bb1-ae11-eda401e1d337">IStreamBufferSink2</a>. <b>IStreamBufferSink3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferSink3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81822768-f627-4324-815f-51d06b4bd7b3">SetAvailableFilter</a>
</td>
<td align="left" width="63%">
Limits how far the Stream Buffer Source filter can seek backward.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferSink3)</code>.




## -see-also




<a href="https://msdn.microsoft.com/ae97e1e2-011d-4bb1-ae11-eda401e1d337">IStreamBufferSink2</a>



<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

