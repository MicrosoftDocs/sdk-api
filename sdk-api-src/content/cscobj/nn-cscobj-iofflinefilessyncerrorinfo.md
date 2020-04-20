---
UID: NN:cscobj.IOfflineFilesSyncErrorInfo
title: IOfflineFilesSyncErrorInfo (cscobj.h)
description: Supplied with the IOfflineFilesSyncProgress::SyncItemResult method to communicate details about the item that experienced a sync error.helpviewer_keywords: ["IOfflineFilesSyncErrorInfo","IOfflineFilesSyncErrorInfo interface [Offline Files]","IOfflineFilesSyncErrorInfo interface [Offline Files]","described","cscobj/IOfflineFilesSyncErrorInfo","of.iofflinefilessyncerrorinfo"]
old-location: of\iofflinefilessyncerrorinfo.htm
tech.root: offlinefiles
ms.assetid: df1dd351-eb18-46e6-b778-852f551adfd1
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncErrorInfo, IOfflineFilesSyncErrorInfo interface [Offline Files], IOfflineFilesSyncErrorInfo interface [Offline Files],described, cscobj/IOfflineFilesSyncErrorInfo, of.iofflinefilessyncerrorinfo
f1_keywords:
- cscobj/IOfflineFilesSyncErrorInfo
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
- IOfflineFilesSyncErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSyncErrorInfo interface


## -description


Supplied with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncprogress-syncitemresult">IOfflineFilesSyncProgress::SyncItemResult</a> method to communicate details about the item that experienced a sync error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncErrorInfo</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileserrorinfo">IOfflineFilesErrorInfo</a>. <b>IOfflineFilesSyncErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getitemchangeflags">GetItemChangeFlags</a>
</td>
<td align="left" width="63%">
Retrieves a value containing a set of flags that describe what changes were encountered during the sync operation associated with the sync error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getlocalinfo">GetLocalInfo</a>
</td>
<td align="left" width="63%">
Retrieves an instance of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the local copy of the item involved in the synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getoriginalinfo">GetOriginalInfo</a>
</td>
<td align="left" width="63%">
Retrieves an instance of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the original copy of the item involved in the synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getremoteinfo">GetRemoteInfo</a>
</td>
<td align="left" width="63%">
Retrieves an instance of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerroriteminfo">IOfflineFilesSyncErrorItemInfo</a> interface containing the file times, size, and attributes of the remote copy of the item involved in the synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-getsyncoperation">GetSyncOperation</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the type of sync operation being performed when the error was encountered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-infoavailable">InfoAvailable</a>
</td>
<td align="left" width="63%">
Indicates whether information was obtained for the local, remote, or original copy of the item during synchronization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerrorinfo-infoenumerated">InfoEnumerated</a>
</td>
<td align="left" width="63%">
Indicates whether information was queried for the local, remote, or original copy of the item during synchronization.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileserrorinfo">IOfflineFilesErrorInfo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

