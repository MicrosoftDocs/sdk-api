---
UID: NN:cscobj.IOfflineFilesItem
title: IOfflineFilesItem
author: windows-sdk-content
description: Represents a single item in the Offline Files cache.
old-location: of\iofflinefilesitem.htm
old-project: OfflineFiles
ms.assetid: 870cf4c4-e757-429d-b6cc-c136ed5aa10e
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IOfflineFilesItem, IOfflineFilesItem interface [Offline Files], IOfflineFilesItem interface [Offline Files],described, cscobj/IOfflineFilesItem, of.iofflinefilesitem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesItem interface


## -description



    Represents a single item in the Offline Files cache. The item may be a server, share, directory or file.  While each item type has a type-specific interface (for example, <a href="https://msdn.microsoft.com/724fabf6-fb27-49c9-8f99-dc61377ac921">IOfflineFilesServerItem</a>), this interface provides the functionality that is common to all items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesItem</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesItem</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/87fbf63a-d103-4c80-b6a7-60784c7350bc">GetItemType</a>
</td>
<td align="left" width="63%">
Returns a type code identifying the type of the item; server, share, directory, or file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fa89807-cd0c-4868-bd65-a8a0a42dff7d">GetParentItem</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IOfflineFilesItem</b> interface for the parent of the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt432961">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves the fully qualified UNC path string for an item in the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03c0fec4-d320-4c46-a07c-3ebbec61cc54">IsMarkedForDeletion</a>
</td>
<td align="left" width="63%">
Determines whether an item has been deleted from the Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b54d6fa-18b6-4ffb-98ce-4cbc44ed5b77">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes any data cached in the object by rereading from the Offline Files cache.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

