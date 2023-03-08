---
UID: NF:fsrmscreen.IFsrmFileScreenBase.get_BlockedFileGroups
title: IFsrmFileScreenBase::get_BlockedFileGroups (fsrmscreen.h)
description: Retrieves or sets the names of the file groups that contain the file name patterns used to specify the files that are blocked by this screen. (Get)
helpviewer_keywords: ["BlockedFileGroups property [File Server Resource Manager]","BlockedFileGroups property [File Server Resource Manager]","IFsrmFileScreenBase interface","IFsrmFileScreenBase interface [File Server Resource Manager]","BlockedFileGroups property","IFsrmFileScreenBase.BlockedFileGroups","IFsrmFileScreenBase.get_BlockedFileGroups","IFsrmFileScreenBase::BlockedFileGroups","IFsrmFileScreenBase::get_BlockedFileGroups","IFsrmFileScreenBase::put_BlockedFileGroups","fs.ifsrmfilescreenbase_blockedfilegroups","fsrm.ifsrmfilescreenbase_blockedfilegroups","fsrmscreen/IFsrmFileScreenBase::BlockedFileGroups","fsrmscreen/IFsrmFileScreenBase::get_BlockedFileGroups","fsrmscreen/IFsrmFileScreenBase::put_BlockedFileGroups","get_BlockedFileGroups"]
old-location: fsrm\ifsrmfilescreenbase_blockedfilegroups.htm
tech.root: fsrm
ms.assetid: 1f75fa45-8de8-42ca-a0f5-5ffe8acea6b8
ms.date: 12/05/2018
ms.keywords: BlockedFileGroups property [File Server Resource Manager], BlockedFileGroups property [File Server Resource Manager],IFsrmFileScreenBase interface, IFsrmFileScreenBase interface [File Server Resource Manager],BlockedFileGroups property, IFsrmFileScreenBase.BlockedFileGroups, IFsrmFileScreenBase.get_BlockedFileGroups, IFsrmFileScreenBase::BlockedFileGroups, IFsrmFileScreenBase::get_BlockedFileGroups, IFsrmFileScreenBase::put_BlockedFileGroups, fs.ifsrmfilescreenbase_blockedfilegroups, fsrm.ifsrmfilescreenbase_blockedfilegroups, fsrmscreen/IFsrmFileScreenBase::BlockedFileGroups, fsrmscreen/IFsrmFileScreenBase::get_BlockedFileGroups, fsrmscreen/IFsrmFileScreenBase::put_BlockedFileGroups, get_BlockedFileGroups
req.header: fsrmscreen.h
req.include-header: FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
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
 - IFsrmFileScreenBase::get_BlockedFileGroups
 - fsrmscreen/IFsrmFileScreenBase::get_BlockedFileGroups
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
 - IFsrmFileScreenBase.BlockedFileGroups
 - IFsrmFileScreenBase.get_BlockedFileGroups
 - IFsrmFileScreenBase.put_BlockedFileGroups
---

# IFsrmFileScreenBase::get_BlockedFileGroups


## -description

Retrieves or sets the names of the file groups that contain the file name patterns used to specify the files that are blocked by this screen.

This property is read/write.

## -parameters

## -remarks

To specify the blocked group names on a new screen, access this property to get an empty collection and then add the group names to the collection.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-file-screens">Using Templates to Define File Screens</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>
