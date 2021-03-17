---
UID: NF:fsrmscreen.IFsrmFileGroupManager.ImportFileGroups
title: IFsrmFileGroupManager::ImportFileGroups (fsrmscreen.h)
description: Imports the specified file groups from an XML string.
helpviewer_keywords: ["FsrmFileGroupManager class [File Server Resource Manager]","ImportFileGroups method","IFsrmFileGroupManager interface [File Server Resource Manager]","ImportFileGroups method","IFsrmFileGroupManager.ImportFileGroups","IFsrmFileGroupManager::ImportFileGroups","ImportFileGroups","ImportFileGroups method [File Server Resource Manager]","ImportFileGroups method [File Server Resource Manager]","FsrmFileGroupManager class","ImportFileGroups method [File Server Resource Manager]","IFsrmFileGroupManager interface","fs.ifsrmfilegroupmanager_importfilegroups","fsrm.ifsrmfilegroupmanager_importfilegroups","fsrmscreen/IFsrmFileGroupManager::ImportFileGroups"]
old-location: fsrm\ifsrmfilegroupmanager_importfilegroups.htm
tech.root: fsrm
ms.assetid: 81f62d49-5fce-4d8c-96b5-506d741c5f77
ms.date: 12/05/2018
ms.keywords: FsrmFileGroupManager class [File Server Resource Manager],ImportFileGroups method, IFsrmFileGroupManager interface [File Server Resource Manager],ImportFileGroups method, IFsrmFileGroupManager.ImportFileGroups, IFsrmFileGroupManager::ImportFileGroups, ImportFileGroups, ImportFileGroups method [File Server Resource Manager], ImportFileGroups method [File Server Resource Manager],FsrmFileGroupManager class, ImportFileGroups method [File Server Resource Manager],IFsrmFileGroupManager interface, fs.ifsrmfilegroupmanager_importfilegroups, fsrm.ifsrmfilegroupmanager_importfilegroups, fsrmscreen/IFsrmFileGroupManager::ImportFileGroups
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
 - IFsrmFileGroupManager::ImportFileGroups
 - fsrmscreen/IFsrmFileGroupManager::ImportFileGroups
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
 - IFsrmFileGroupManager.ImportFileGroups
 - FsrmFileGroupManager.ImportFileGroups
---

# IFsrmFileGroupManager::ImportFileGroups


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Imports the specified file groups from an XML string.

## -parameters

### -param serializedFileGroups [in]

An XML string that represents one or more file groups.

### -param fileGroupNamesArray [in]

A <b>VARIANT</b> that contains a <b>SAFEARRAY</b> of the names 
      of the file groups to import. If <b>NULL</b>, the method imports all file groups.

### -param fileGroups [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
       that contains a collection of file groups.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroupimported">IFsrmFileGroupImported</a> interface.

To add the file groups to FSRM, call the 
       <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a> 
       method.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilegroupmanager">FsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroupmanager">IFsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>