---
UID: NN:cscobj.IOfflineFilesSyncErrorItemInfo
title: IOfflineFilesSyncErrorItemInfo (cscobj.h)
description: Provides file attributes, time information, and file size for an item associated with a sync error.
old-location: of\iofflinefilessyncerroriteminfo.htm
tech.root: offlinefiles
ms.assetid: 0af039a6-f0dd-4117-a174-38d32cfc0220
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncErrorItemInfo, IOfflineFilesSyncErrorItemInfo interface [Offline Files], IOfflineFilesSyncErrorItemInfo interface [Offline Files],described, cscobj/IOfflineFilesSyncErrorItemInfo, of.iofflinefilessyncerroriteminfo
ms.topic: interface
f1_keywords:
- cscobj/IOfflineFilesSyncErrorItemInfo
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
- IOfflineFilesSyncErrorItemInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesSyncErrorItemInfo interface


## -description


Provides file attributes, time information, and file size for an item associated with a sync error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSyncErrorItemInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesSyncErrorItemInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSyncErrorItemInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerroriteminfo-getfileattributes">GetFileAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the Win32 file attributes for the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerroriteminfo-getfilesize">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the item in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilessyncerroriteminfo-getfiletimes">GetFileTimes</a>
</td>
<td align="left" width="63%">
Retrieves the last-write and change times for the item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

