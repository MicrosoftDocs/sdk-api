---
UID: NN:comsvcs.IObjectContextInfo2
title: IObjectContextInfo2 (comsvcs.h)
author: windows-sdk-content
description: Provides additional information about an object's context. This interface extends the IObjectContextInfo interface.
old-location: cos\iobjectcontextinfo2.htm
tech.root: cossdk
ms.assetid: 21e078d2-ba93-4118-b1d1-3b4b6e0e28a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IObjectContextInfo2, IObjectContextInfo2 interface [COM+], IObjectContextInfo2 interface [COM+],described, _cos_IObjectContextInfo2, comsvcs/IObjectContextInfo2, cos.iobjectcontextinfo2
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectContextInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectContextInfo2 interface


## -description


Provides additional information about an object's context. This interface extends the <a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectContextInfo2</b> interface inherits from <b>IObjectContextInfo</b>. <b>IObjectContextInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectContextInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45cf882a-7a46-4106-a03d-c87c0b52477e">GetApplicationId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e20e02c8-23ad-4234-9f20-4e8cae2e9279">GetApplicationInstanceId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application instance of the current object context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/090afcec-d124-4b7c-822a-ecb56f9037a6">GetPartitionId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the partition of the current object context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a>
 

 

