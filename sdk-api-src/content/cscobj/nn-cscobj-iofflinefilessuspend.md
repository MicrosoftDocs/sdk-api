---
UID: NN:cscobj.IOfflineFilesSuspend
title: IOfflineFilesSuspend (cscobj.h)
description: Suspends or releases a share root or directory tree in the Offline Files cache.helpviewer_keywords: ["IOfflineFilesSuspend","IOfflineFilesSuspend interface [Offline Files]","IOfflineFilesSuspend interface [Offline Files]","described","cscobj/IOfflineFilesSuspend","of.iofflinefilessuspend"]
old-location: of\iofflinefilessuspend.htm
tech.root: offlinefiles
ms.assetid: 697018c4-7cce-480a-b078-993cdac32bf5
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSuspend, IOfflineFilesSuspend interface [Offline Files], IOfflineFilesSuspend interface [Offline Files],described, cscobj/IOfflineFilesSuspend, of.iofflinefilessuspend
f1_keywords:
- cscobj/IOfflineFilesSuspend
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
- IOfflineFilesSuspend
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSuspend interface


## -description


Suspends or releases a share root or directory tree in the Offline Files cache. A suspended tree is always offline and is never synchronized automatically by the Offline Files service.  It may, however, be synchronized by the user through Windows Explorer, through Sync Center, or by code calling the Offline Files API.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSuspend</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesSuspend</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSuspend</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessuspend-suspendroot">SuspendRoot</a>
</td>
<td align="left" width="63%">
Suspend or release a share root or directory tree.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

