---
UID: NF:fsrmquota.IFsrmQuotaManager.CreateQuota
title: IFsrmQuotaManager::CreateQuota (fsrmquota.h)
description: Creates a quota for the specified directory.
helpviewer_keywords: ["CreateQuota","CreateQuota method [File Server Resource Manager]","CreateQuota method [File Server Resource Manager]","FsrmQuotaManager class","CreateQuota method [File Server Resource Manager]","IFsrmQuotaManager interface","CreateQuota method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","FsrmQuotaManager class [File Server Resource Manager]","CreateQuota method","IFsrmQuotaManager interface [File Server Resource Manager]","CreateQuota method","IFsrmQuotaManager.CreateQuota","IFsrmQuotaManager::CreateQuota","IFsrmQuotaManagerEx interface [File Server Resource Manager]","CreateQuota method","IFsrmQuotaManagerEx::CreateQuota","fs.ifsrmquotamanager_createquota","fsrm.ifsrmquotamanager_createquota","fsrmquota/IFsrmQuotaManager::CreateQuota","fsrmquota/IFsrmQuotaManagerEx::CreateQuota"]
old-location: fsrm\ifsrmquotamanager_createquota.htm
tech.root: fsrm
ms.assetid: 09f0b952-e24f-4388-8e82-6b34145f9ad4
ms.date: 12/05/2018
ms.keywords: CreateQuota, CreateQuota method [File Server Resource Manager], CreateQuota method [File Server Resource Manager],FsrmQuotaManager class, CreateQuota method [File Server Resource Manager],IFsrmQuotaManager interface, CreateQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],CreateQuota method, IFsrmQuotaManager interface [File Server Resource Manager],CreateQuota method, IFsrmQuotaManager.CreateQuota, IFsrmQuotaManager::CreateQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],CreateQuota method, IFsrmQuotaManagerEx::CreateQuota, fs.ifsrmquotamanager_createquota, fsrm.ifsrmquotamanager_createquota, fsrmquota/IFsrmQuotaManager::CreateQuota, fsrmquota/IFsrmQuotaManagerEx::CreateQuota
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
 - IFsrmQuotaManager::CreateQuota
 - fsrmquota/IFsrmQuotaManager::CreateQuota
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
 - IFsrmQuotaManager.CreateQuota
 - IFsrmQuotaManagerEx.CreateQuota
 - FsrmQuotaManager.CreateQuota
---

# IFsrmQuotaManager::CreateQuota


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Creates a quota for the specified directory.

## -parameters

### -param path [in]

The local directory path to which the quota applies. The string is limited to 260 characters.

### -param quota [out]

An <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a> interface to the newly created quota 
      object. Use this interface to define the quota. To add the quota to FSRM, call 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmQuota::Commit</a> method.

## -returns

The method returns the following return values.

## -remarks

The quota applies to the directory and all its subdirectories (recursively). Quotas specified on directories 
    higher in the directory tree further restrict the quota specified on this directory.

If the quota specifies the <b>FsrmQuotaFlags_Enforce</b>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-get_quotaflags">quota flag</a>, the file IO is blocked when the quota 
    is exceeded, but there are no actions taken, such as a command being run or a report generated. To perform actions 
    when the quota is exceeded, <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-addthreshold">create a threshold</a> 
    and specify an action to run. To perform the action when the quota is exceeded, set the threshold to 
    100 (percent).


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/defining-a-quota">Defining a Quota</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>