---
UID: NF:fsrmscreen.IFsrmFileGroupManager.CreateFileGroup
title: IFsrmFileGroupManager::CreateFileGroup (fsrmscreen.h)
description: Creates a file group object.
helpviewer_keywords: ["CreateFileGroup","CreateFileGroup method [File Server Resource Manager]","CreateFileGroup method [File Server Resource Manager]","FsrmFileGroupManager class","CreateFileGroup method [File Server Resource Manager]","IFsrmFileGroupManager interface","FsrmFileGroupManager class [File Server Resource Manager]","CreateFileGroup method","IFsrmFileGroupManager interface [File Server Resource Manager]","CreateFileGroup method","IFsrmFileGroupManager.CreateFileGroup","IFsrmFileGroupManager::CreateFileGroup","fs.ifsrmfilegroupmanager_createfilegroup","fsrm.ifsrmfilegroupmanager_createfilegroup","fsrmscreen/IFsrmFileGroupManager::CreateFileGroup"]
old-location: fsrm\ifsrmfilegroupmanager_createfilegroup.htm
tech.root: fsrm
ms.assetid: 7e2c3672-fbb9-4da5-9e20-25c66213843c
ms.date: 12/05/2018
ms.keywords: CreateFileGroup, CreateFileGroup method [File Server Resource Manager], CreateFileGroup method [File Server Resource Manager],FsrmFileGroupManager class, CreateFileGroup method [File Server Resource Manager],IFsrmFileGroupManager interface, FsrmFileGroupManager class [File Server Resource Manager],CreateFileGroup method, IFsrmFileGroupManager interface [File Server Resource Manager],CreateFileGroup method, IFsrmFileGroupManager.CreateFileGroup, IFsrmFileGroupManager::CreateFileGroup, fs.ifsrmfilegroupmanager_createfilegroup, fsrm.ifsrmfilegroupmanager_createfilegroup, fsrmscreen/IFsrmFileGroupManager::CreateFileGroup
req.header: fsrmscreen.h
req.include-header: 
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
 - IFsrmFileGroupManager::CreateFileGroup
 - fsrmscreen/IFsrmFileGroupManager::CreateFileGroup
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
 - IFsrmFileGroupManager.CreateFileGroup
 - FsrmFileGroupManager.CreateFileGroup
---

# IFsrmFileGroupManager::CreateFileGroup


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Creates a file group object.

## -parameters

### -param fileGroup [out]

An <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroup">IFsrmFileGroup</a> interface to the new file group. To 
      add the file group to FSRM, call 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileGroup::Commit</a> method.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilegroupmanager">FsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroupmanager">IFsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>