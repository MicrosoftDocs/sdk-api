---
UID: NN:comsvcs.IObjPool
title: IObjPool
author: windows-sdk-content
description: Represents the key to each object in the transaction resource pool.
old-location: cos\iobjpool.htm
old-project: cossdk
ms.assetid: d3730a37-933b-4705-b787-4b8bb728a278
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: IObjPool, IObjPool interface [COM+], IObjPool interface [COM+],described, _cos_IObjPool, comsvcs/IObjPool, cos.iobjpool
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjPool
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IObjPool interface


## -description


Represents the key to each object in the transaction resource pool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjPool</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjPool</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjPool</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24a80209-6ed8-426e-a645-463393a3a37e">PutEndTx</a>
</td>
<td align="left" width="63%">
Destroys the pooled object when the transaction ends.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/602842ce-abb1-4830-99b3-d361d18ac074">ITransactionProperty</a>



<a href="https://msdn.microsoft.com/bf7ca849-6025-4358-bf2d-629d80e06a04">ITransactionResourcePool</a>
 

 

