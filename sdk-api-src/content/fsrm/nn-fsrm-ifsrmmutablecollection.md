---
UID: NN:fsrm.IFsrmMutableCollection
title: IFsrmMutableCollection
author: windows-sdk-content
description: Used to manage a collection of FSRM objects that can have objects added to or removed from the collection.
old-location: fsrm\ifsrmmutablecollection.htm
old-project: fsrm
ms.assetid: e41f01ef-5dd2-4066-82cd-45b57578c9bb
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IFsrmMutableCollection, IFsrmMutableCollection interface [File Server Resource Manager], IFsrmMutableCollection interface [File Server Resource Manager],described, fs.ifsrmmutablecollection, fsrm.ifsrmmutablecollection, fsrm/IFsrmMutableCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmMutableCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmMutableCollection interface


## -description


Used to manage a collection of FSRM objects that can have objects added to or removed from the collection.

The following properties return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/242a86ab-9dec-4106-9a49-70c12cc6de91">IFsrmFileGroup::Members</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c3c2ff78-db1a-44df-a7af-15c4a6c4b22d">IFsrmFileGroup::NonMembers</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1f75fa45-8de8-42ca-a0f5-5ffe8acea6b8">IFsrmFileScreenBase::BlockedFileGroups</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e02070dd-a51d-4572-a282-4e5a151cd987">IFsrmFileScreenException::AllowedFileGroups</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmMutableCollection</b> interface inherits from <a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>. <b>IFsrmMutableCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmMutableCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate <b>IFsrmMutableCollection</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified object from the collection using an index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f6fc4c-72fe-47c8-91c5-21987fa91848">RemoveById</a>
</td>
<td align="left" width="63%">
Removes the specified object from the collection using an object identifier.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6a0c5d8b-5fed-4c55-971c-43430e3c6a8d">IFsrmCollection</a>
 

 

