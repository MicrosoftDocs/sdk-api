---
UID: NN:cscobj.IOfflineFilesChangeInfo
title: IOfflineFilesChangeInfo (cscobj.h)
author: windows-sdk-content
description: Represents the information associated with local changes made to an item while working offline.
old-location: of\iofflinefileschangeinfo.htm
tech.root: offlinefiles
ms.assetid: 0ece6120-bd5d-4e3d-b71f-7aa9a51a1568
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesChangeInfo, IOfflineFilesChangeInfo interface [Offline Files], IOfflineFilesChangeInfo interface [Offline Files],described, cscobj/IOfflineFilesChangeInfo, of.iofflinefileschangeinfo
ms.topic: interface
f1_keywords: 
 - "cscobj/IOfflineFilesChangeInfo"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesChangeInfo interface


## -description


Represents the information associated with local changes made to an item while working offline.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesChangeInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesChangeInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileschangeinfo-iscreatedoffline">IsCreatedOffline</a>
</td>
<td align="left" width="63%">
Determines whether an item was created in the Offline Files cache while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileschangeinfo-isdeletedoffline">IsDeletedOffline</a>
</td>
<td align="left" width="63%">
Determines whether an item has been deleted from the Offline Files cache while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileschangeinfo-isdirty">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an item in the Offline Files cache has been modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileschangeinfo-islocallymodifiedattributes">IsLocallyModifiedAttributes</a>
</td>
<td align="left" width="63%">
Determines whether one or more of an item's attributes were modified while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileschangeinfo-islocallymodifieddata">IsLocallyModifiedData</a>
</td>
<td align="left" width="63%">
Determines whether an item's data was modified while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileschangeinfo-islocallymodifiedtime">IsLocallyModifiedTime</a>
</td>
<td align="left" width="63%">
Determines whether one or more of an item's time values were modified while working offline.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

