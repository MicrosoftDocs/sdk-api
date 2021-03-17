---
UID: NF:fsrmscreen.IFsrmFileGroupManager.GetFileGroup
title: IFsrmFileGroupManager::GetFileGroup (fsrmscreen.h)
description: Retrieves the specified file group from FSRM.
helpviewer_keywords: ["FsrmFileGroupManager class [File Server Resource Manager]","GetFileGroup method","GetFileGroup","GetFileGroup method [File Server Resource Manager]","GetFileGroup method [File Server Resource Manager]","FsrmFileGroupManager class","GetFileGroup method [File Server Resource Manager]","IFsrmFileGroupManager interface","IFsrmFileGroupManager interface [File Server Resource Manager]","GetFileGroup method","IFsrmFileGroupManager.GetFileGroup","IFsrmFileGroupManager::GetFileGroup","fs.ifsrmfilegroupmanager_getfilegroup","fsrm.ifsrmfilegroupmanager_getfilegroup","fsrmscreen/IFsrmFileGroupManager::GetFileGroup"]
old-location: fsrm\ifsrmfilegroupmanager_getfilegroup.htm
tech.root: fsrm
ms.assetid: 14b61b2b-a20e-4895-bfbe-40e9dfe0c496
ms.date: 12/05/2018
ms.keywords: FsrmFileGroupManager class [File Server Resource Manager],GetFileGroup method, GetFileGroup, GetFileGroup method [File Server Resource Manager], GetFileGroup method [File Server Resource Manager],FsrmFileGroupManager class, GetFileGroup method [File Server Resource Manager],IFsrmFileGroupManager interface, IFsrmFileGroupManager interface [File Server Resource Manager],GetFileGroup method, IFsrmFileGroupManager.GetFileGroup, IFsrmFileGroupManager::GetFileGroup, fs.ifsrmfilegroupmanager_getfilegroup, fsrm.ifsrmfilegroupmanager_getfilegroup, fsrmscreen/IFsrmFileGroupManager::GetFileGroup
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
 - IFsrmFileGroupManager::GetFileGroup
 - fsrmscreen/IFsrmFileGroupManager::GetFileGroup
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
 - IFsrmFileGroupManager.GetFileGroup
 - FsrmFileGroupManager.GetFileGroup
---

# IFsrmFileGroupManager::GetFileGroup


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Retrieves the specified file group from FSRM.

## -parameters

### -param name [in]

The name of the file group to retrieve. The string is limited to 4,000 characters.

### -param fileGroup [out]

An <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroup">IFsrmFileGroup</a> interface to the retrieved file 
      group.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilegroupmanager">FsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroupmanager">IFsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>