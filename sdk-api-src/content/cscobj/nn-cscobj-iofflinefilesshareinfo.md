---
UID: NN:cscobj.IOfflineFilesShareInfo
title: IOfflineFilesShareInfo (cscobj.h)
description: Presents share-specific information about cached items.
helpviewer_keywords: ["IOfflineFilesShareInfo","IOfflineFilesShareInfo interface [Offline Files]","IOfflineFilesShareInfo interface [Offline Files]","described","cscobj/IOfflineFilesShareInfo","of.iofflinefilesshareinfo"]
old-location: of\iofflinefilesshareinfo.htm
tech.root: offlinefiles
ms.assetid: 9647aae3-06ca-4813-8243-3d0fb794802d
ms.date: 12/05/2018
ms.keywords: IOfflineFilesShareInfo, IOfflineFilesShareInfo interface [Offline Files], IOfflineFilesShareInfo interface [Offline Files],described, cscobj/IOfflineFilesShareInfo, of.iofflinefilesshareinfo
f1_keywords:
- cscobj/IOfflineFilesShareInfo
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
- IOfflineFilesShareInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesShareInfo interface


## -description


Presents share-specific information about cached items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesShareInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesShareInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesShareInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesshareinfo-getsharecachingmode">GetShareCachingMode</a>
</td>
<td align="left" width="63%">
Retrieves the caching mode configuration of the closest ancestor share to the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesshareinfo-getshareitem">GetShareItem</a>
</td>
<td align="left" width="63%">
Finds the cache item representing the closest ancestor share to the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesshareinfo-issharedfsjunction">IsShareDfsJunction</a>
</td>
<td align="left" width="63%">
Determines whether the share item is a DFS junction or a shared folder on a server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

