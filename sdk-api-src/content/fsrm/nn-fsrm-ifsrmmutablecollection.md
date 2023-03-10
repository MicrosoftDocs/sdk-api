---
UID: NN:fsrm.IFsrmMutableCollection
title: IFsrmMutableCollection (fsrm.h)
description: Used to manage a collection of FSRM objects that can have objects added to or removed from the collection.
helpviewer_keywords: ["IFsrmMutableCollection","IFsrmMutableCollection interface [File Server Resource Manager]","IFsrmMutableCollection interface [File Server Resource Manager]","described","fs.ifsrmmutablecollection","fsrm.ifsrmmutablecollection","fsrm/IFsrmMutableCollection"]
old-location: fsrm\ifsrmmutablecollection.htm
tech.root: fsrm
ms.assetid: e41f01ef-5dd2-4066-82cd-45b57578c9bb
ms.date: 12/05/2018
ms.keywords: IFsrmMutableCollection, IFsrmMutableCollection interface [File Server Resource Manager], IFsrmMutableCollection interface [File Server Resource Manager],described, fs.ifsrmmutablecollection, fsrm.ifsrmmutablecollection, fsrm/IFsrmMutableCollection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmMutableCollection
 - fsrm/IFsrmMutableCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmMutableCollection
---

# IFsrmMutableCollection interface


## -description

Used to manage a collection of FSRM objects that can have objects added to or removed from the collection.

The following properties return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroup-get_members">IFsrmFileGroup::Members</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroup-get_nonmembers">IFsrmFileGroup::NonMembers</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-get_blockedfilegroups">IFsrmFileScreenBase::BlockedFileGroups</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenexception-get_allowedfilegroups">IFsrmFileScreenException::AllowedFileGroups</a>
</li>
</ul>

## -inheritance

The <b>IFsrmMutableCollection</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>. <b>IFsrmMutableCollection</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a>
