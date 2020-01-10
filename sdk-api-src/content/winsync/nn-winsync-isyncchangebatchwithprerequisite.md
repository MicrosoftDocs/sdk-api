---
UID: NN:winsync.ISyncChangeBatchWithPrerequisite
title: ISyncChangeBatchWithPrerequisite (winsync.h)
description: Represents metadata about a change batch that is based on the prerequisite knowledge associated with the change batch.
old-location: winsync\isyncchangebatchwithprerequisite.htm
tech.root: winsync
ms.assetid: 29d767cf-3261-4550-8b28-5d3950b8ded1
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchWithPrerequisite, ISyncChangeBatchWithPrerequisite interface [Windows Sync], ISyncChangeBatchWithPrerequisite interface [Windows Sync],described, winsync.isyncchangebatchwithprerequisite, winsync/ISyncChangeBatchWithPrerequisite
f1_keywords:
- winsync/ISyncChangeBatchWithPrerequisite
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchWithPrerequisite interface


## -description


Represents metadata about a change batch that is based on the prerequisite knowledge associated with the change batch.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchWithPrerequisite</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase</a>. <b>ISyncChangeBatchWithPrerequisite</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchwithprerequisite-getlearnedforgottenknowledge">GetLearnedForgottenKnowledge</a>
</td>
<td align="left" width="63%">
Gets the forgotten knowledge that the destination replica learns when the destination provider applies all the changes in this change batch during recovery synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchwithprerequisite-getlearnedknowledgewithprerequisite">GetLearnedKnowledgeWithPrerequisite</a>
</td>
<td align="left" width="63%">
Gets the knowledge that the destination replica learns when the destination provider applies all the changes in this change batch, based on the prerequisite knowledge of the change batch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchwithprerequisite-setprerequisiteknowledge">SetPrerequisiteKnowledge</a>
</td>
<td align="left" width="63%">
Sets the minimum knowledge that a destination provider is required to have to process this change batch.

</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeBatchWithPrerequisite</b> object can be obtained by passing <b>IID_ISyncChangeBatchWithPrerequisite</b> to the <b>QueryInterface</b> method of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase</a> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

