---
UID: NF:fsrmquota.IFsrmQuotaManager.CreateQuotaCollection
title: IFsrmQuotaManager::CreateQuotaCollection (fsrmquota.h)
description: Creates an empty collection to which you can add quotas.
helpviewer_keywords: ["CreateQuotaCollection","CreateQuotaCollection method [File Server Resource Manager]","CreateQuotaCollection method [File Server Resource Manager]","FsrmQuotaManager class","CreateQuotaCollection method [File Server Resource Manager]","IFsrmQuotaManager interface","CreateQuotaCollection method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","FsrmQuotaManager class [File Server Resource Manager]","CreateQuotaCollection method","IFsrmQuotaManager interface [File Server Resource Manager]","CreateQuotaCollection method","IFsrmQuotaManager.CreateQuotaCollection","IFsrmQuotaManager::CreateQuotaCollection","IFsrmQuotaManagerEx interface [File Server Resource Manager]","CreateQuotaCollection method","IFsrmQuotaManagerEx::CreateQuotaCollection","fs.ifsrmquotamanager_createquotacollection","fsrm.ifsrmquotamanager_createquotacollection","fsrmquota/IFsrmQuotaManager::CreateQuotaCollection","fsrmquota/IFsrmQuotaManagerEx::CreateQuotaCollection"]
old-location: fsrm\ifsrmquotamanager_createquotacollection.htm
tech.root: fsrm
ms.assetid: 88656cb9-1e72-4f82-ac09-fbb3c8a36afc
ms.date: 12/05/2018
ms.keywords: CreateQuotaCollection, CreateQuotaCollection method [File Server Resource Manager], CreateQuotaCollection method [File Server Resource Manager],FsrmQuotaManager class, CreateQuotaCollection method [File Server Resource Manager],IFsrmQuotaManager interface, CreateQuotaCollection method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],CreateQuotaCollection method, IFsrmQuotaManager interface [File Server Resource Manager],CreateQuotaCollection method, IFsrmQuotaManager.CreateQuotaCollection, IFsrmQuotaManager::CreateQuotaCollection, IFsrmQuotaManagerEx interface [File Server Resource Manager],CreateQuotaCollection method, IFsrmQuotaManagerEx::CreateQuotaCollection, fs.ifsrmquotamanager_createquotacollection, fsrm.ifsrmquotamanager_createquotacollection, fsrmquota/IFsrmQuotaManager::CreateQuotaCollection, fsrmquota/IFsrmQuotaManagerEx::CreateQuotaCollection
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
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
 - IFsrmQuotaManager::CreateQuotaCollection
 - fsrmquota/IFsrmQuotaManager::CreateQuotaCollection
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
 - IFsrmQuotaManager.CreateQuotaCollection
 - IFsrmQuotaManagerEx.CreateQuotaCollection
 - FsrmQuotaManager.CreateQuotaCollection
---

# IFsrmQuotaManager::CreateQuotaCollection


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Creates an empty collection to which you can add quotas.

## -parameters

### -param collection [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
      to the newly created collection. To add an object to the collection, call the 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmmutablecollection-add">IFsrmMutableCollection::Add</a> method.

## -returns

The method returns the following return values.

## -remarks

Using the collection to add more than one quota provides better performance than adding individual quotas. 
    After adding the quotas to the collection, call the 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a> 
    method.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>