---
UID: NN:cscobj.IOfflineFilesSyncConflictHandler
title: IOfflineFilesSyncConflictHandler (cscobj.h)
description: Used by a client calling the IOfflineFilesCache::Synchronize method to prescribe a conflict resolution strategy for sync conflicts as they are detected.
helpviewer_keywords: ["IOfflineFilesSyncConflictHandler","IOfflineFilesSyncConflictHandler interface [Offline Files]","IOfflineFilesSyncConflictHandler interface [Offline Files]","described","cscobj/IOfflineFilesSyncConflictHandler","of.iofflinefilessyncconflicthandler"]
old-location: of\iofflinefilessyncconflicthandler.htm
tech.root: offlinefiles
ms.assetid: f3d5ed0e-727d-43e1-9d29-2a0a71bb8a64
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncConflictHandler, IOfflineFilesSyncConflictHandler interface [Offline Files], IOfflineFilesSyncConflictHandler interface [Offline Files],described, cscobj/IOfflineFilesSyncConflictHandler, of.iofflinefilessyncconflicthandler
f1_keywords:
- cscobj/IOfflineFilesSyncConflictHandler
dev_langs:
- c++
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CscSvc.dll
- CscObj.dll
api_name:
- IOfflineFilesSyncConflictHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSyncConflictHandler interface


## -description


Used by a client calling the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a> method to prescribe a conflict resolution strategy for sync conflicts as they are detected.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncConflictHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesSyncConflictHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncConflictHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncconflicthandler-resolveconflict">ResolveConflict</a>
</td>
<td align="left" width="63%">
Provides a resolution decision for a sync conflict.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

