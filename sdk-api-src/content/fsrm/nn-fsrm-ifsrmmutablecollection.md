---
UID: NN:fsrm.IFsrmMutableCollection
title: IFsrmMutableCollection (fsrm.h)

description: Used to manage a collection of FSRM objects that can have objects added to or removed from the collection.
old-location: fsrm\ifsrmmutablecollection.htm
tech.root: fsrm
ms.assetid: e41f01ef-5dd2-4066-82cd-45b57578c9bb

ms.date: 12/05/2018
ms.keywords: IFsrmMutableCollection, IFsrmMutableCollection interface [File Server Resource Manager], IFsrmMutableCollection interface [File Server Resource Manager],described, fs.ifsrmmutablecollection, fsrm.ifsrmmutablecollection, fsrm/IFsrmMutableCollection
ms.topic: interface
f1_keywords: 
 - "fsrm/IFsrmMutableCollection"
dev_langs:
 - c++
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmMutableCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmMutableCollection interface


## -description


Used to manage a collection of FSRM objects that can have objects added to or removed from the collection.

The following properties return this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroup-get_members">IFsrmFileGroup::Members</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroup-get_nonmembers">IFsrmFileGroup::NonMembers</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-get_blockedfilegroups">IFsrmFileScreenBase::BlockedFileGroups</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenexception-get_allowedfilegroups">IFsrmFileScreenException::AllowedFileGroups</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmMutableCollection</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>. <b>IFsrmMutableCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmmutablecollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmmutablecollection-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate <b>IFsrmMutableCollection</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmmutablecollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified object from the collection using an index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmmutablecollection-removebyid">RemoveById</a>
</td>
<td align="left" width="63%">
Removes the specified object from the collection using an object identifier.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>
 

 

