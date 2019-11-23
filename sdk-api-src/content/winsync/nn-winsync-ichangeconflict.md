---
UID: NN:winsync.IChangeConflict
title: IChangeConflict (winsync.h)

description: Represents a conflict between two items.
old-location: winsync\ichangeconflict.htm
tech.root: winsync
ms.assetid: b0089d3d-a1e6-4662-9e79-4c0b22c08d7f

ms.date: 12/05/2018
ms.keywords: IChangeConflict, IChangeConflict interface [Windows Sync], IChangeConflict interface [Windows Sync],described, winsync.ichangeconflict, winsync/IChangeConflict
ms.topic: interface
f1_keywords: 
 - "winsync/IChangeConflict"
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
 - IChangeConflict
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IChangeConflict interface


## -description


Represents a conflict between two items.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IChangeConflict</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IChangeConflict</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IChangeConflict</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getdestinationproviderconflictingchange">GetDestinationProviderConflictingChange</a>
</td>
<td align="left" width="63%">
Gets the change metadata from the destination provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getdestinationproviderconflictingdata">GetDestinationProviderConflictingData</a>
</td>
<td align="left" width="63%">
Gets an object that can be used to retrieve item data for the change item from the destination replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getresolveactionforchange">GetResolveActionForChange</a>
</td>
<td align="left" width="63%">
Gets the conflict resolution action for the conflict.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getresolveactionforchangeunit">GetResolveActionForChangeUnit</a>
</td>
<td align="left" width="63%">
Gets the conflict resolution action for the conflicting change unit change.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getsourceproviderconflictingchange">GetSourceProviderConflictingChange</a>
</td>
<td align="left" width="63%">
Gets the change metadata from the source provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-getsourceproviderconflictingdata">GetSourceProviderConflictingData</a>
</td>
<td align="left" width="63%">
Gets an object that can be used to retrieve item data for the change item from the source replica.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-setresolveactionforchange">SetResolveActionForChange</a>
</td>
<td align="left" width="63%">
Sets a conflict resolution action for the conflict.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeconflict-setresolveactionforchangeunit">SetResolveActionForChangeUnit</a>
</td>
<td align="left" width="63%">
Sets a conflict resolution action for the conflicting change unit change.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

