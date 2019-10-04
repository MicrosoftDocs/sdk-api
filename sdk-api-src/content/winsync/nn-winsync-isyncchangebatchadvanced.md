---
UID: NN:winsync.ISyncChangeBatchAdvanced
title: ISyncChangeBatchAdvanced (winsync.h)
author: windows-sdk-content
description: Represents additional information about a set of changes.
old-location: winsync\isyncchangebatchadvanced.htm
tech.root: winsync
ms.assetid: b78bc885-ed4e-4c83-ad1b-043c5b226337
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncChangeBatchAdvanced, ISyncChangeBatchAdvanced interface [Windows Sync], ISyncChangeBatchAdvanced interface [Windows Sync],described, winsync.isyncchangebatchadvanced, winsync/ISyncChangeBatchAdvanced
ms.topic: interface
f1_keywords: 
 - "winsync/ISyncChangeBatchAdvanced"
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
 - ISyncChangeBatchAdvanced
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncChangeBatchAdvanced interface


## -description


Represents additional information about a set of changes.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncChangeBatchAdvanced</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncChangeBatchAdvanced</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncChangeBatchAdvanced</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchadvanced-convertfullenumerationchangebatchtoregularchangebatch">ConvertFullEnumerationChangeBatchToRegularChangeBatch</a>
</td>
<td align="left" width="63%">
Converts an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch</a> object to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch</a> object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchadvanced-getbatchlevelknowledgeshouldbeapplied">GetBatchLevelKnowledgeShouldBeApplied</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the learned knowledge for the batch must be saved after the batch is applied to the destination replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchadvanced-getfilterinfo">GetFilterInfo</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo</a> that was specified when the change batch was created.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncchangebatchadvanced-getupperbounditemid">GetUpperBoundItemId</a>
</td>
<td align="left" width="63%">
Gets the highest item ID that is represented in the knowledge of any group in the change batch.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/">RemapKnowledges</a>
</td>
<td align="left" width="63%">
Remaps all knowledge objects that are contained in the change batch so that they are relative to the replica key map of the specified knowledge.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncChangeBatchAdvanced</b> object can be obtained by passing <b>IID_ISyncChangeBatchAdvanced</b> to the <b>QueryInterface</b> method of a change batch object, such as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch</a> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase">ISyncChangeBatchBase Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchbase2">ISyncChangeBatchBase2 Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchwithprerequisite">ISyncChangeBatchWithPrerequisite Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfullenumerationchangebatch">ISyncFullEnumerationChangeBatch Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

