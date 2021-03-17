---
UID: NF:fsrmscreen.IFsrmFileGroupManager.EnumFileGroups
title: IFsrmFileGroupManager::EnumFileGroups (fsrmscreen.h)
description: Enumerates the file groups in FSRM.
helpviewer_keywords: ["EnumFileGroups","EnumFileGroups method [File Server Resource Manager]","EnumFileGroups method [File Server Resource Manager]","FsrmFileGroupManager class","EnumFileGroups method [File Server Resource Manager]","IFsrmFileGroupManager interface","FsrmFileGroupManager class [File Server Resource Manager]","EnumFileGroups method","IFsrmFileGroupManager interface [File Server Resource Manager]","EnumFileGroups method","IFsrmFileGroupManager.EnumFileGroups","IFsrmFileGroupManager::EnumFileGroups","fs.ifsrmfilegroupmanager_enumfilegroups","fsrm.ifsrmfilegroupmanager_enumfilegroups","fsrmscreen/IFsrmFileGroupManager::EnumFileGroups"]
old-location: fsrm\ifsrmfilegroupmanager_enumfilegroups.htm
tech.root: fsrm
ms.assetid: 317eb6cf-7bcc-4042-a7b7-05efac84a0c2
ms.date: 12/05/2018
ms.keywords: EnumFileGroups, EnumFileGroups method [File Server Resource Manager], EnumFileGroups method [File Server Resource Manager],FsrmFileGroupManager class, EnumFileGroups method [File Server Resource Manager],IFsrmFileGroupManager interface, FsrmFileGroupManager class [File Server Resource Manager],EnumFileGroups method, IFsrmFileGroupManager interface [File Server Resource Manager],EnumFileGroups method, IFsrmFileGroupManager.EnumFileGroups, IFsrmFileGroupManager::EnumFileGroups, fs.ifsrmfilegroupmanager_enumfilegroups, fsrm.ifsrmfilegroupmanager_enumfilegroups, fsrmscreen/IFsrmFileGroupManager::EnumFileGroups
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
 - IFsrmFileGroupManager::EnumFileGroups
 - fsrmscreen/IFsrmFileGroupManager::EnumFileGroups
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
 - IFsrmFileGroupManager.EnumFileGroups
 - FsrmFileGroupManager.EnumFileGroups
---

# IFsrmFileGroupManager::EnumFileGroups


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Enumerates the file groups in FSRM.

## -parameters

### -param options [in]

One or more options for enumerating the file groups. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param fileGroups [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
       that contains a collection of file groups. Each item of the collection is a 
       <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the 
       <b>pdispVal</b> member of the variant for the 
       <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroup">IFsrmFileGroup</a> interface.

The collection contains only committed file groups; the collection will not contain newly created file groups 
       that have not been committed.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilegroupmanager">FsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroupmanager">IFsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>