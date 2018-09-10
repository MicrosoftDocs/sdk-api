---
UID: NN:cscobj.IOfflineFilesChangeInfo
title: IOfflineFilesChangeInfo
author: windows-sdk-content
description: Represents the information associated with local changes made to an item while working offline.
old-location: of\iofflinefileschangeinfo.htm
tech.root: offlinefiles
ms.assetid: 0ece6120-bd5d-4e3d-b71f-7aa9a51a1568
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesChangeInfo, IOfflineFilesChangeInfo interface [Offline Files], IOfflineFilesChangeInfo interface [Offline Files],described, cscobj/IOfflineFilesChangeInfo, of.iofflinefileschangeinfo
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
 - IOfflineFilesChangeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesChangeInfo interface


## -description


Represents the information associated with local changes made to an item while working offline.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesChangeInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesChangeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesChangeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2074df23-a2dd-45ea-9ef4-5619cebebe31">IsCreatedOffline</a>
</td>
<td align="left" width="63%">
Determines whether an item was created in the Offline Files cache while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6a739f3-0c3d-46f1-8548-89be0660ef59">IsDeletedOffline</a>
</td>
<td align="left" width="63%">
Determines whether an item has been deleted from the Offline Files cache while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47b3bae2-d0fb-4e15-a03f-c9d5001e8786">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an item in the Offline Files cache has been modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c45a04cd-a1cf-4239-9a77-07b6b67121e8">IsLocallyModifiedAttributes</a>
</td>
<td align="left" width="63%">
Determines whether one or more of an item's attributes were modified while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d27999af-147e-4c1b-be89-58191292337d">IsLocallyModifiedData</a>
</td>
<td align="left" width="63%">
Determines whether an item's data was modified while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b88bf6d-f5a7-48e3-8c0a-41a8f6fba91f">IsLocallyModifiedTime</a>
</td>
<td align="left" width="63%">
Determines whether one or more of an item's time values were modified while working offline.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

