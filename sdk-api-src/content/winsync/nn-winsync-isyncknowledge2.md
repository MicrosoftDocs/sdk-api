---
UID: NN:winsync.ISyncKnowledge2
title: ISyncKnowledge2 (winsync.h)
description: Represents additional information about the knowledge that a replica has about its item store.
old-location: winsync\isyncknowledge2.htm
tech.root: winsync
ms.assetid: 1acbae32-8fa6-4c1e-95f6-30aca483c966
ms.date: 12/05/2018
ms.keywords: ISyncKnowledge2, ISyncKnowledge2 interface [Windows Sync], ISyncKnowledge2 interface [Windows Sync],described, winsync.isyncknowledge2, winsync/ISyncKnowledge2
ms.topic: interface
f1_keywords:
- winsync/ISyncKnowledge2
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
- ISyncKnowledge2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncKnowledge2 interface


## -description


Represents additional information about the knowledge that a replica has about its item store.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncKnowledge2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge</a>. <b>ISyncKnowledge2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncKnowledge2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-comparetoknowledgecookie">CompareToKnowledgeCookie</a>
</td>
<td align="left" width="63%">
Performs a fast comparison between the specified knowledge cookie and this knowledge object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-complement">Complement</a>
</td>
<td align="left" width="63%">
Returns the knowledge that is contained in this object but that is not contained in the specified knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-containsknowledgeforchangeunit">ContainsKnowledgeForChangeUnit</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge of the specified change unit is known by this knowledge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-containsknowledgeforitem">ContainsKnowledgeForItem</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge of the specified item is known by this knowledge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-getidparameters">GetIdParameters</a>
</td>
<td align="left" width="63%">
Gets the ID format schema of the provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-getinspector">GetInspector</a>
</td>
<td align="left" width="63%">
Returns an object that can be used to retrieve the contents of the knowledge object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-getknowledgecookie">GetKnowledgeCookie</a>
</td>
<td align="left" width="63%">
Gets a lightweight, read-only representation of this knowledge object that can be used for fast comparisons.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-getlowestuncontainedid">GetLowestUncontainedId</a>
</td>
<td align="left" width="63%">
Returns the lowest item ID that is contained in the specified knowledge and that is not contained in this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-getminimumsupportedversion">GetMinimumSupportedVersion</a>
</td>
<td align="left" width="63%">
Gets the minimum supported version of Microsoft Sync Framework components that can be used with this object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-getstatistics">GetStatistics</a>
</td>
<td align="left" width="63%">
Gets the specified statistic data that is contained in this object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-intersectswithknowledge">IntersectsWithKnowledge</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge intersects with this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-projectontocolumnset">ProjectOntoColumnSet</a>
</td>
<td align="left" width="63%">
Returns the knowledge for the specified set of change units for all the items that are contained in this object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-projectontoknowledgewithprerequisite">ProjectOntoKnowledgeWithPrerequisite</a>
</td>
<td align="left" width="63%">
Returns knowledge about the knowledge fragments that are specified by the template knowledge, when the template knowledge contains the prerequisite knowledge for the specified fragments. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncknowledge2-serializewithoptions">SerializeWithOptions</a>
</td>
<td align="left" width="63%">
Serializes the knowledge object data to a byte array based on the specified version and serialization options.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncKnowledge2</b> object can be obtained by passing <b>IID_ISyncKnowledge2</b> to the <b>QueryInterface</b> method of an <b>ISyncKnowledge</b> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

