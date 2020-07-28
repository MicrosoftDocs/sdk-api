---
UID: NN:cscobj.IOfflineFilesItemContainer
title: IOfflineFilesItemContainer (cscobj.h)
description: Used to access item enumeration functionality in the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesItemContainer","IOfflineFilesItemContainer interface [Offline Files]","IOfflineFilesItemContainer interface [Offline Files]","described","cscobj/IOfflineFilesItemContainer","of.iofflinefilesitemcontainer"]
old-location: of\iofflinefilesitemcontainer.htm
tech.root: of
ms.assetid: 328ad076-cafd-461e-8085-7fca65063fa0
ms.date: 12/05/2018
ms.keywords: IOfflineFilesItemContainer, IOfflineFilesItemContainer interface [Offline Files], IOfflineFilesItemContainer interface [Offline Files],described, cscobj/IOfflineFilesItemContainer, of.iofflinefilesitemcontainer
f1_keywords:
- cscobj/IOfflineFilesItemContainer
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
- IOfflineFilesItemContainer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesItemContainer interface


## -description


Used to access item enumeration functionality in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesItemContainer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesItemContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesItemContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemcontainer-enumitems">EnumItems</a>
</td>
<td align="left" width="63%">
Returns an enumerator of child items for the cache item implementing this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitemcontainer-enumitemsex">EnumItemsEx</a>
</td>
<td align="left" width="63%">
Returns an enumerator of child items for the cache item implementing this method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

