---
UID: NN:winsync.ISyncChangeBatchBase
title: ISyncChangeBatchBase
author: windows-sdk-content
description: Represents metadata for a set of changes.
old-location: winsync\isyncchangebatchbase.htm
old-project: winsync
ms.assetid: 14ca01a1-04eb-4282-adf0-e775d6ff0801
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncChangeBatchBase, ISyncChangeBatchBase interface [Windows Sync], ISyncChangeBatchBase interface [Windows Sync],described, winsync.isyncchangebatchbase, winsync/ISyncChangeBatchBase
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChangeBatchBase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchBase interface


## -description


Represents metadata for a set of changes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchBase</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncChangeBatchBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatchBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb5b5a35-70d9-413d-8bf6-7003fe7681c8">AddItemMetadataToGroup</a>
</td>
<td align="left" width="63%">
Adds a specified item change to the group that is currently open.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/093c0014-fa03-4609-a38f-5e69a3d3c4d6">BeginOrderedGroup</a>
</td>
<td align="left" width="63%">
Opens an ordered group in the change batch. This group is ordered by item ID.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d53ef88e-0d1f-4328-988c-c759391ca28c">EndOrderedGroup</a>
</td>
<td align="left" width="63%">
Closes a previously opened ordered group in the change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af979d71-1eb4-463d-8e90-27a985ea289d">GetChangeEnumerator</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/c3f27c6d-4fc1-420c-afc1-0bd2bdbd6ab2">IEnumSyncChanges</a> object that enumerates the item changes in this change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74b82fde-c492-4d5f-a680-62b836420cee">GetIsLastBatch</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the changes in this change batch are the last batch of a synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cef04646-71a7-489d-9beb-fe87bb949218">GetLearnedKnowledge</a>
</td>
<td align="left" width="63%">
Gets the knowledge that the destination replica learns when the destination provider applies the changes in this change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd078725-7fd8-4d6c-9b43-f6741b03f1e6">GetPrerequisiteKnowledge</a>
</td>
<td align="left" width="63%">
Gets the minimum knowledge that a destination provider is required to have to process this change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c1d3cf3-4d84-43c0-91cc-fbc418b8cb20">GetRemainingWorkEstimateForSession</a>
</td>
<td align="left" width="63%">
Gets the estimate of the remaining work for the session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/309b2c83-4480-421c-ae90-9cbe7ac11055">GetSourceForgottenKnowledge</a>
</td>
<td align="left" width="63%">
Gets the forgotten knowledge of the source replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4abf4027-814a-461d-b179-b2510abccc5e">GetWorkEstimateForBatch</a>
</td>
<td align="left" width="63%">
Gets the work estimate for the batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/785a763c-99a2-45d1-b42b-9673aedc5c5d">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the change batch to an array of bytes.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7619b446-5c71-4533-8af6-15f06dda3c87">SetLastBatch</a>
</td>
<td align="left" width="63%">
Sets a flag that indicates there are no more changes to be enumerated in the synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f73d13d9-244e-4ec1-aacd-047331b13a4d">SetRemainingWorkEstimateForSession</a>
</td>
<td align="left" width="63%">
Sets the estimate of the remaining work for the batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da88dd49-4b11-444c-8137-212f8c673122">SetWorkEstimateForBatch</a>
</td>
<td align="left" width="63%">
Sets the work estimate for the session.


</td>
</tr>
</table> 


## -remarks



<b>ISyncChangeBatchBase</b> is the base interface for change batches. Typically, it is overridden by a derived interface, such as <a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch</a> for a knowledge synchronization, and <a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch</a> for a full enumeration synchronization.




## -see-also




<a href="https://msdn.microsoft.com/c3f27c6d-4fc1-420c-afc1-0bd2bdbd6ab2">IEnumSyncChanges Interface</a>



<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/b78bc885-ed4e-4c83-ad1b-043c5b226337">ISyncChangeBatchAdvanced Interface</a>



<a href="https://msdn.microsoft.com/45f10ed0-b3ce-41f5-b2d9-9166bff2abec">ISyncChangeBatchBase2 Interface</a>



<a href="https://msdn.microsoft.com/29d767cf-3261-4550-8b28-5d3950b8ded1">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

