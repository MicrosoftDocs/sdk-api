---
UID: NN:winsync.ISupportLastWriteTime
title: ISupportLastWriteTime (winsync.h)
description: Represents a synchronization provider that is able to report the date and time when an item or change unit was last changed. This ability is useful to an application that implements last-writer-wins conflict resolution.
old-location: winsync\isupportlastwritetime.htm
tech.root: winsync
ms.assetid: b95e2b75-add7-4cdd-b18a-21918e9c8c08
ms.date: 12/05/2018
ms.keywords: ISupportLastWriteTime, ISupportLastWriteTime interface [Windows Sync], ISupportLastWriteTime interface [Windows Sync],described, winsync.isupportlastwritetime, winsync/ISupportLastWriteTime
f1_keywords:
- winsync/ISupportLastWriteTime
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
- ISupportLastWriteTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISupportLastWriteTime interface


## -description


Represents a synchronization provider that is able to report the date and time when an item or change unit was last changed. This ability is useful to an application that implements last-writer-wins conflict resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISupportLastWriteTime</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISupportLastWriteTime</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISupportLastWriteTime</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportlastwritetime-getchangeunitchangetime">GetChangeUnitChangeTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the specified change unit was last changed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportlastwritetime-getitemchangetime">GetItemChangeTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the specified item was last changed.


</td>
</tr>
</table> 


## -remarks



This interface is typically implemented by a provider. If a provider implements this interface, it must return a pointer to it when <b>IID_ISupportLastWriteTime</b> is passed to the <b>QueryInterface</b> method of its data transfer interface. The data transfer interface is the interface that a provider returns in response to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynchronousdataretriever-loadchangedata">ISynchronousDataRetriever::LoadChangeData</a> method.

To implement last-writer-wins conflict resolution, an application typically performs the following steps:

<ol>
<li>Registers an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback</a> object to receive conflict notifications.</li>
<li>In the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isynccallback-onconflict">ISyncCallback::OnConflict</a> method, calls <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getdestinationproviderconflictingdata">IChangeConflict::GetDestinationProviderConflictingData</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getsourceproviderconflictingdata">IChangeConflict::GetSourceProviderConflictingData</a> on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict</a> object to get the data transfer interfaces for the conflicting changes.</li>
<li>Passes <b>IID_ISupportLastWriteTime</b> to the <b>QueryInterface</b> method of each data transfer interface to get the <b>ISupportLastWriteTime</b> objects that represent the conflicting changes.</li>
<li>Calls <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportlastwritetime-getitemchangetime">GetItemChangeTime</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isupportlastwritetime-getchangeunitchangetime">GetChangeUnitChangeTime</a> on the <b>ISupportLastWriteTime</b> objects to get the last date and time the changes were made.</li>
<li>Compares the date and time values to determine which change was made last.</li>
<li>Indicates which change to keep by using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-setresolveactionforchange">IChangeConflict::SetResolveActionForChange</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-setresolveactionforchangeunit">IChangeConflict::SetResolveActionForChangeUnit</a> method.</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-ichangeconflict">IChangeConflict Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isynccallback">ISyncCallback Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

