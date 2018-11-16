---
UID: NN:cscobj.IOfflineFilesChangeInfo
title: IOfflineFilesChangeInfo
author: windows-sdk-content
description: Represents the information associated with local changes made to an item while working offline.
old-location: of\iofflinefileschangeinfo.htm
tech.root: OfflineFiles
ms.assetid: 0ece6120-bd5d-4e3d-b71f-7aa9a51a1568
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesChangeInfo, IOfflineFilesChangeInfo interface [Offline Files], IOfflineFilesChangeInfo interface [Offline Files],described, cscobj/IOfflineFilesChangeInfo, of.iofflinefileschangeinfo
ms.prod: windows-hardware
ms.technology: windows-devices
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesChangeInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesChangeInfo</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Bb530505(v=VS.85).aspx">IsCreatedOffline</a>
</td>
<td align="left" width="63%">
Determines whether an item was created in the Offline Files cache while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530506(v=VS.85).aspx">IsDeletedOffline</a>
</td>
<td align="left" width="63%">
Determines whether an item has been deleted from the Offline Files cache while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530507(v=VS.85).aspx">IsDirty</a>
</td>
<td align="left" width="63%">
Determines whether an item in the Offline Files cache has been modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530508(v=VS.85).aspx">IsLocallyModifiedAttributes</a>
</td>
<td align="left" width="63%">
Determines whether one or more of an item's attributes were modified while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530509(v=VS.85).aspx">IsLocallyModifiedData</a>
</td>
<td align="left" width="63%">
Determines whether an item's data was modified while working offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530510(v=VS.85).aspx">IsLocallyModifiedTime</a>
</td>
<td align="left" width="63%">
Determines whether one or more of an item's time values were modified while working offline.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

