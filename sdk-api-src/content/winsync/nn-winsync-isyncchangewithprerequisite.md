---
UID: NN:winsync.ISyncChangeWithPrerequisite
title: ISyncChangeWithPrerequisite
author: windows-sdk-content
description: Represents metadata about a change that is based on the prerequisite knowledge that is associated with the change.
old-location: winsync\isyncchangewithprerequisite.htm
old-project: winsync
ms.assetid: 7650fc2c-fe2d-4cb1-a22a-433c90c5cb8d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncChangeWithPrerequisite, ISyncChangeWithPrerequisite interface [Windows Sync], ISyncChangeWithPrerequisite interface [Windows Sync],described, winsync.isyncchangewithprerequisite, winsync/ISyncChangeWithPrerequisite
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChangeWithPrerequisite
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeWithPrerequisite interface


## -description


Represents metadata about a change that is based on the prerequisite knowledge that is associated with the change.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeWithPrerequisite</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncChangeWithPrerequisite</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5717f126-9383-4304-88eb-1d0fa3bb762f">GetLearnedKnowledgeWithPrerequisite</a>
</td>
<td align="left" width="63%">
Gets the knowledge that the destination replica learns when the destination provider applies this change, based on the prerequisite knowledge that is associated with the change.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48aa9436-b708-4dad-9201-d57988baf749">GetPrerequisiteKnowledge</a>
</td>
<td align="left" width="63%">
Gets the minimum knowledge that a destination provider is required to have to process this change.

</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeWithPrerequisite</b> object can be obtained by passing <b>IID_ ISyncChangeWithPrerequisite</b> to the <b>QueryInterface</b> method of an <a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange</a> object.




## -see-also




<a href="https://msdn.microsoft.com/0cd29977-8d02-4a1e-b63f-783cc10021ee">ISyncChange Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

