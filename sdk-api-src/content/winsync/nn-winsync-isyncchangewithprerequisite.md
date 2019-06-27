---
UID: NN:winsync.ISyncChangeWithPrerequisite
title: ISyncChangeWithPrerequisite (winsync.h)
author: windows-sdk-content
description: Represents metadata about a change that is based on the prerequisite knowledge that is associated with the change.
old-location: winsync\isyncchangewithprerequisite.htm
tech.root: winsync
ms.assetid: 7650fc2c-fe2d-4cb1-a22a-433c90c5cb8d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncChangeWithPrerequisite, ISyncChangeWithPrerequisite interface [Windows Sync], ISyncChangeWithPrerequisite interface [Windows Sync],described, winsync.isyncchangewithprerequisite, winsync/ISyncChangeWithPrerequisite
ms.topic: interface
f1_keywords: 
 - "winsync/ISyncChangeWithPrerequisite"
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
 - ISyncChangeWithPrerequisite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeWithPrerequisite interface


## -description


Represents metadata about a change that is based on the prerequisite knowledge that is associated with the change.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeWithPrerequisite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChangeWithPrerequisite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeWithPrerequisite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangewithprerequisite-getlearnedknowledgewithprerequisite">GetLearnedKnowledgeWithPrerequisite</a>
</td>
<td align="left" width="63%">
Gets the knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangewithprerequisite-getprerequisiteknowledge">GetPrerequisiteKnowledge</a>
</td>
<td align="left" width="63%">
Gets the minimum knowledge that a destination provider is required to have to process this change.

</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeWithPrerequisite</b> object can be obtained by passing <b>IID_ ISyncChangeWithPrerequisite</b> to the <b>QueryInterface</b> method of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange</a> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchange">ISyncChange Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

