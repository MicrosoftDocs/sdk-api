---
UID: NN:cscobj.IOfflineFilesCache2
title: IOfflineFilesCache2 (cscobj.h)
description: Implements the RenameItemEx method.
helpviewer_keywords: ["IOfflineFilesCache2","IOfflineFilesCache2 interface [Offline Files]","IOfflineFilesCache2 interface [Offline Files]","described","cscobj/IOfflineFilesCache2","of.iofflinefilescache2"]
old-location: of\iofflinefilescache2.htm
tech.root: of
ms.assetid: B4E2C2B0-AA6B-4657-8711-E5057720AF15
ms.date: 12/05/2018
ms.keywords: IOfflineFilesCache2, IOfflineFilesCache2 interface [Offline Files], IOfflineFilesCache2 interface [Offline Files],described, cscobj/IOfflineFilesCache2, of.iofflinefilescache2
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1
req.target-min-winversvr: Windows Server 2008 R2 with SP1
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
 - IOfflineFilesCache2
 - cscobj/IOfflineFilesCache2
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
 - IOfflineFilesCache2
---

# IOfflineFilesCache2 interface


## -description

Implements the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache2-renameitemex">RenameItemEx</a> method.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesCache2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>. <b>IOfflineFilesCache2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesCache2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache2-renameitemex">RenameItemEx</a>
</td>
<td align="left" width="63%">
Renames an item in the cache. This method is identical to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-renameitem">IOfflineFilesCache::RenameItem</a> method, except that it will attempt to do the rename operation right away.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>

