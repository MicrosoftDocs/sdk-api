---
UID: NN:winsync.ISyncFullEnumerationChangeBatch
title: ISyncFullEnumerationChangeBatch
author: windows-sdk-content
description: Represents the metadata for a set of changes that is created as part of a recovery synchronization.
old-location: winsync\isyncfullenumerationchangebatch.htm
old-project: winsync
ms.assetid: 9086991d-03e3-4f2c-ad03-c1f554fe32ce
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISyncFullEnumerationChangeBatch, ISyncFullEnumerationChangeBatch interface [Windows Sync], ISyncFullEnumerationChangeBatch interface [Windows Sync],described, winsync.isyncfullenumerationchangebatch, winsync/ISyncFullEnumerationChangeBatch
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
 - ISyncFullEnumerationChangeBatch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncFullEnumerationChangeBatch interface


## -description


Represents the metadata for a set of changes that is created as part of a recovery synchronization.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncFullEnumerationChangeBatch</b> interface inherits from <a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase</a>. <b>ISyncFullEnumerationChangeBatch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncFullEnumerationChangeBatch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0cc8564-f87a-4642-b085-5149c85279dd">GetClosedLowerBoundItemId</a>
</td>
<td align="left" width="63%">
Gets the closed lower bound on item IDs that require destination versions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b06b01b2-2f31-4117-92eb-e72e31a2f20b">GetClosedUpperBoundItemId</a>
</td>
<td align="left" width="63%">
Gets the closed upper bound on item IDs that require destination versions.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8eb9fdbf-b1ce-4acf-837f-01d693940790">GetLearnedKnowledgeAfterRecoveryComplete</a>
</td>
<td align="left" width="63%">
Gets the knowledge the destination replica will learn after it applies all the changes in the recovery synchronization.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

