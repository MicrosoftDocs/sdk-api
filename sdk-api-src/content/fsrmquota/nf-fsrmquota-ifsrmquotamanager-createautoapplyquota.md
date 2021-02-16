---
UID: NF:fsrmquota.IFsrmQuotaManager.CreateAutoApplyQuota
title: IFsrmQuotaManager::CreateAutoApplyQuota (fsrmquota.h)
description: Creates an automatic quota for the specified directory.
helpviewer_keywords: ["CreateAutoApplyQuota","CreateAutoApplyQuota method [File Server Resource Manager]","CreateAutoApplyQuota method [File Server Resource Manager]","FsrmQuotaManager class","CreateAutoApplyQuota method [File Server Resource Manager]","IFsrmQuotaManager interface","CreateAutoApplyQuota method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","FsrmQuotaManager class [File Server Resource Manager]","CreateAutoApplyQuota method","IFsrmQuotaManager interface [File Server Resource Manager]","CreateAutoApplyQuota method","IFsrmQuotaManager.CreateAutoApplyQuota","IFsrmQuotaManager::CreateAutoApplyQuota","IFsrmQuotaManagerEx interface [File Server Resource Manager]","CreateAutoApplyQuota method","IFsrmQuotaManagerEx::CreateAutoApplyQuota","fs.ifsrmquotamanager_createautoapplyquota","fsrm.ifsrmquotamanager_createautoapplyquota","fsrmquota/IFsrmQuotaManager::CreateAutoApplyQuota","fsrmquota/IFsrmQuotaManagerEx::CreateAutoApplyQuota"]
old-location: fsrm\ifsrmquotamanager_createautoapplyquota.htm
tech.root: fsrm
ms.assetid: faaa55ca-a0b1-4cd4-9c73-20d80879b10c
ms.date: 12/05/2018
ms.keywords: CreateAutoApplyQuota, CreateAutoApplyQuota method [File Server Resource Manager], CreateAutoApplyQuota method [File Server Resource Manager],FsrmQuotaManager class, CreateAutoApplyQuota method [File Server Resource Manager],IFsrmQuotaManager interface, CreateAutoApplyQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],CreateAutoApplyQuota method, IFsrmQuotaManager interface [File Server Resource Manager],CreateAutoApplyQuota method, IFsrmQuotaManager.CreateAutoApplyQuota, IFsrmQuotaManager::CreateAutoApplyQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],CreateAutoApplyQuota method, IFsrmQuotaManagerEx::CreateAutoApplyQuota, fs.ifsrmquotamanager_createautoapplyquota, fsrm.ifsrmquotamanager_createautoapplyquota, fsrmquota/IFsrmQuotaManager::CreateAutoApplyQuota, fsrmquota/IFsrmQuotaManagerEx::CreateAutoApplyQuota
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
 - IFsrmQuotaManager::CreateAutoApplyQuota
 - fsrmquota/IFsrmQuotaManager::CreateAutoApplyQuota
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
 - IFsrmQuotaManager.CreateAutoApplyQuota
 - IFsrmQuotaManagerEx.CreateAutoApplyQuota
 - FsrmQuotaManager.CreateAutoApplyQuota
---

# IFsrmQuotaManager::CreateAutoApplyQuota


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Creates an automatic quota for the specified directory.

## -parameters

### -param quotaTemplateName [in]

The name of a template from which to derive the quota; automatic quotas must derive from a template. The 
      string is limited to 4,000 characters.

### -param path [in]

The local directory path to which the quota applies. The string is limited to 260 characters.

### -param quota [out]

An <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmautoapplyquota">IFsrmAutoApplyQuota</a> interface to the newly 
      created quota object. The specified template is used to initialize the quota. Use this interface to change the 
      quota and to exclude specific subdirectories from the quota. To add the quota to FSRM, call 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmAutoApplyQuota::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

When you save the automatic quota, FSRM creates quotas for all existing subdirectories under the specified 
    directory that do not already contain a quota. When a new subdirectory is created under the specified directory, 
    FSRM uses the properties of the automatic quota to create a quota for the new subdirectory.

If you are creating both the automatic quota and the subdirectories at the same time, you should first 
    create the subdirectories and then create the automatic quota because it provides better performance.


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-quota">Defining a Quota</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>