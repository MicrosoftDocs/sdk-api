---
UID: NN:winsync.ISyncSessionState
title: ISyncSessionState (winsync.h)

description: Represents information about the current synchronization session.
old-location: winsync\isyncsessionstate.htm
tech.root: winsync
ms.assetid: 9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e

ms.date: 12/05/2018
ms.keywords: ISyncSessionState, ISyncSessionState interface [Windows Sync], ISyncSessionState interface [Windows Sync],described, winsync.isyncsessionstate, winsync/ISyncSessionState
ms.topic: interface
f1_keywords: 
 - "winsync/ISyncSessionState"
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
 - ISyncSessionState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncSessionState interface


## -description


Represents information about the current synchronization session.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncSessionState</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncSessionState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncSessionState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate-getforgottenknowledgerecoveryrangeend">GetForgottenKnowledgeRecoveryRangeEnd</a>
</td>
<td align="left" width="63%">
Gets the upper bound of the recovery range when the session is performing forgotten knowledge recovery.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate-getforgottenknowledgerecoveryrangestart">GetForgottenKnowledgeRecoveryRangeStart</a>
</td>
<td align="left" width="63%">
Gets the lower bound of the recovery range when the session is performing forgotten knowledge recovery.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate-getinfoforchangeapplication">GetInfoForChangeApplication</a>
</td>
<td align="left" width="63%">
Retrieves stored data for a serialized change applier.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate-iscanceled">IsCanceled</a>
</td>
<td align="left" width="63%">
Indicates whether the synchronization session has been canceled.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate-loadinfofromchangeapplication">LoadInfoFromChangeApplication</a>
</td>
<td align="left" width="63%">
Stores data for a serialized change applier.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate-onprogress">OnProgress</a>
</td>
<td align="left" width="63%">
Reports progress periodically during the synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate-setforgottenknowledgerecoveryrange">SetForgottenKnowledgeRecoveryRange</a>
</td>
<td align="left" width="63%">
Sets the recovery range when the session is performing forgotten knowledge recovery.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

