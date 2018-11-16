---
UID: NN:winsync.ISyncChangeBatchWithPrerequisite
title: ISyncChangeBatchWithPrerequisite
author: windows-sdk-content
description: Represents metadata about a change batch that is based on the prerequisite knowledge associated with the change batch.
old-location: winsync\isyncchangebatchwithprerequisite.htm
tech.root: winsync
ms.assetid: 29d767cf-3261-4550-8b28-5d3950b8ded1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ISyncChangeBatchWithPrerequisite, ISyncChangeBatchWithPrerequisite interface [Windows Sync], ISyncChangeBatchWithPrerequisite interface [Windows Sync],described, winsync.isyncchangebatchwithprerequisite, winsync/ISyncChangeBatchWithPrerequisite
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeBatchWithPrerequisite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChangeBatchWithPrerequisite interface


## -description


Represents metadata about a change batch that is based on the prerequisite knowledge associated with the change batch.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchWithPrerequisite</b> interface inherits from <a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase</a>. <b>ISyncChangeBatchWithPrerequisite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatchWithPrerequisite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e7a9f72-7d5e-4ef8-824a-d7623b71cfb5">GetLearnedForgottenKnowledge</a>
</td>
<td align="left" width="63%">
Gets the forgotten knowledge that the destination replica learns when the destination provider applies all the changes in this change batch during recovery synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/691f2cc1-9acb-4474-b20a-31bb7810372e">GetLearnedKnowledgeWithPrerequisite</a>
</td>
<td align="left" width="63%">
Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a138dbd9-e498-40bf-9490-690103afbf0f">SetPrerequisiteKnowledge</a>
</td>
<td align="left" width="63%">
Sets the minimum knowledge that a destination provider is required to have to process this change batch.

</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeBatchWithPrerequisite</b> object can be obtained by passing <b>IID_ISyncChangeBatchWithPrerequisite</b> to the <b>QueryInterface</b> method of an <a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase</a> object.




## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

