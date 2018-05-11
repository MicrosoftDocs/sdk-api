---
UID: NN:winsync.ISynchronousDataRetriever
title: ISynchronousDataRetriever
author: windows-driver-content
description: Represents the mechanism by which the destination provider retrieves item data from the source provider.
old-location: winsync\isynchronousdataretriever.htm
old-project: winsync
ms.assetid: d59a5198-5878-4a48-b6c4-042afc36054d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISynchronousDataRetriever, ISynchronousDataRetriever interface [Windows Sync], ISynchronousDataRetriever interface [Windows Sync],described, winsync.isynchronousdataretriever, winsync/ISynchronousDataRetriever
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISynchronousDataRetriever
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISynchronousDataRetriever interface


## -description


Represents the mechanism by which the destination provider retrieves item data from the source provider.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISynchronousDataRetriever</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISynchronousDataRetriever</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISynchronousDataRetriever</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98273eec-93fd-44ae-a1c9-cf85790dfc1d">GetIdParameters</a>
</td>
<td align="left" width="63%">
Gets the ID format schema of the provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae309301-3810-4785-b4f2-a55fbdf819d8">LoadChangeData</a>
</td>
<td align="left" width="63%">
Retrieves item data for a change.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

