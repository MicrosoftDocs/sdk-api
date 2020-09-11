---
UID: NN:cscobj.IOfflineFilesSyncProgress
title: IOfflineFilesSyncProgress (cscobj.h)
description: Used to report progress back to the caller during synchronization and synchronization-related operations.
helpviewer_keywords: ["IOfflineFilesSyncProgress","IOfflineFilesSyncProgress interface [Offline Files]","IOfflineFilesSyncProgress interface [Offline Files]","described","cscobj/IOfflineFilesSyncProgress","of.iofflinefilessyncprogress"]
old-location: of\iofflinefilessyncprogress.htm
tech.root: of
ms.assetid: 7fc5ff29-be9d-4fad-96a8-94058bb708fa
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncProgress, IOfflineFilesSyncProgress interface [Offline Files], IOfflineFilesSyncProgress interface [Offline Files],described, cscobj/IOfflineFilesSyncProgress, of.iofflinefilessyncprogress
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesSyncProgress
 - cscobj/IOfflineFilesSyncProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSyncProgress
---

# IOfflineFilesSyncProgress interface


## -description

Used to report progress back to the caller during synchronization and 
    synchronization-related operations. This interface inherits from 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>.  For a description of 
    inherited methods, see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncProgress</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>. <b>IOfflineFilesSyncProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitembegin">SyncItemBegin</a>
</td>
<td align="left" width="63%">
Reports that a synchronization operation on an item is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitemresult">SyncItemResult</a>
</td>
<td align="left" width="63%">
Reports that an item has been processed during the synchronization operation.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesprogress">IOfflineFilesProgress</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>

