---
UID: NN:winsync.IAsynchronousDataRetriever
title: IAsynchronousDataRetriever
author: windows-sdk-content
description: Represents the mechanism by which the destination provider asynchronously retrieves item data from the source provider.
old-location: winsync\iasynchronousdataretriever.htm
old-project: winsync
ms.assetid: 38f07582-908b-430e-a886-c0fc24b807ef
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAsynchronousDataRetriever, IAsynchronousDataRetriever interface [Windows Sync], IAsynchronousDataRetriever interface [Windows Sync],described, winsync.iasynchronousdataretriever, winsync/IAsynchronousDataRetriever
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IAsynchronousDataRetriever
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAsynchronousDataRetriever interface


## -description


Represents the mechanism by which the destination provider asynchronously retrieves item data from the source provider.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsynchronousDataRetriever</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAsynchronousDataRetriever</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAsynchronousDataRetriever</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20f42e0d-dacb-4362-843b-8bc2fb664203">GetIdParameters</a>
</td>
<td align="left" width="63%">
Gets the ID format schema of the provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5e73504-1f9e-4a58-9bd9-2c184372b970">LoadChangeData</a>
</td>
<td align="left" width="63%">
Retrieves item data for a change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4148db4a-a460-40ca-863a-861065f89c5c">RegisterCallback</a>
</td>
<td align="left" width="63%">
Registers a callback interface that will be called by the <b>IAsynchronousDataRetriever</b> object when an asynchronous method finishes processing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb7b1457-03aa-47e0-9e61-6195706a0fcd">RevokeCallback</a>
</td>
<td align="left" width="63%">
Indicates that the <b>IAsynchronousDataRetriever</b>  object must no longer use the specified callback interface and must release any references to it.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

