---
UID: NN:cscobj.IOfflineFilesItem
title: IOfflineFilesItem (cscobj.h)
author: windows-sdk-content
description: Represents a single item in the Offline Files cache.
old-location: of\iofflinefilesitem.htm
tech.root: offlinefiles
ms.assetid: 870cf4c4-e757-429d-b6cc-c136ed5aa10e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesItem, IOfflineFilesItem interface [Offline Files], IOfflineFilesItem interface [Offline Files],described, cscobj/IOfflineFilesItem, of.iofflinefilesitem
ms.topic: interface
f1_keywords: ["cscobj/IOfflineFilesItem"]
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
 - IOfflineFilesItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesItem interface


## -description


Represents a single item in the Offline Files cache. The item may be a server, share, directory or file.  While each item type has a type-specific interface (for example, <a href="https://docs.microsoft.com/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesserveritem">IOfflineFilesServerItem</a>), this interface provides the functionality that is common to all items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitem-getitemtype">GetItemType</a>
</td>
<td align="left" width="63%">
Returns a type code identifying the type of the item; server, share, directory, or file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitem-getparentitem">GetParentItem</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IOfflineFilesItem</b> interface for the parent of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitem-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves the fully qualified UNC path string for an item in the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitem-ismarkedfordeletion">IsMarkedForDeletion</a>
</td>
<td align="left" width="63%">
Determines whether an item has been deleted from the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesitem-refresh">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes any data cached in the object by rereading from the Offline Files cache.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

