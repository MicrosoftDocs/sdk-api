---
UID: NN:winsync.ISyncChangeBatch
title: ISyncChangeBatch
author: windows-sdk-content
description: Represents metadata for a set of changes.
old-location: winsync\isyncchangebatch.htm
old-project: winsync
ms.assetid: 3bfd5cf2-ca73-490e-84a7-506c198b3d7c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISyncChangeBatch, ISyncChangeBatch interface [Windows Sync], ISyncChangeBatch interface [Windows Sync],described, winsync.isyncchangebatch, winsync/ISyncChangeBatch
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
 - ISyncChangeBatch
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatch interface


## -description


Represents metadata for a set of changes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatch</b> interface inherits from <b>ISyncChangeBatchBase</b>. <b>ISyncChangeBatch</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatch</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7f83c35-754a-4211-b893-2df6f65266a6">AddLoggedConflict</a>
</td>
<td align="left" width="63%">
Adds metadata that represents a conflict to the change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d44451a-9150-4b2c-b126-d4fa90c2e192">BeginUnorderedGroup</a>
</td>
<td align="left" width="63%">
Opens an unordered group in the change batch. Item changes in this group can be in any order.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca9c37ca-6aa0-437d-b933-ca7d943e4ef2">EndUnorderedGroup</a>
</td>
<td align="left" width="63%">
Closes a previously opened unordered group in the change batch.


</td>
</tr>
</table> 


## -remarks



Change batches are used by synchronization providers to communicate metadata for item changes from a source provider to a destination provider. The source provider enumerates changes and adds a specified number of them to a change batch. The change batch is then sent to the destination provider. The destination provider enumerates the changes in the change batch and applies them to its item store.




## -see-also




<a href="https://msdn.microsoft.com/b78bc885-ed4e-4c83-ad1b-043c5b226337">ISyncChangeBatchAdvanced Interface</a>



<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/45f10ed0-b3ce-41f5-b2d9-9166bff2abec">ISyncChangeBatchBase2 Interface</a>



<a href="https://msdn.microsoft.com/29d767cf-3261-4550-8b28-5d3950b8ded1">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

