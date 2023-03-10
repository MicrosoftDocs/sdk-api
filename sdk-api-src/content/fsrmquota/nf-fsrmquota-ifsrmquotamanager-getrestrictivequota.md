---
UID: NF:fsrmquota.IFsrmQuotaManager.GetRestrictiveQuota
title: IFsrmQuotaManager::GetRestrictiveQuota (fsrmquota.h)
description: Retrieves the most restrictive quota for the specified path.
helpviewer_keywords: ["FsrmQuotaManager class [File Server Resource Manager]","GetRestrictiveQuota method","GetRestrictiveQuota","GetRestrictiveQuota method [File Server Resource Manager]","GetRestrictiveQuota method [File Server Resource Manager]","FsrmQuotaManager class","GetRestrictiveQuota method [File Server Resource Manager]","IFsrmQuotaManager interface","GetRestrictiveQuota method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","IFsrmQuotaManager interface [File Server Resource Manager]","GetRestrictiveQuota method","IFsrmQuotaManager.GetRestrictiveQuota","IFsrmQuotaManager::GetRestrictiveQuota","IFsrmQuotaManagerEx interface [File Server Resource Manager]","GetRestrictiveQuota method","IFsrmQuotaManagerEx::GetRestrictiveQuota","fs.ifsrmquotamanager_getrestrictivequota","fsrm.ifsrmquotamanager_getrestrictivequota","fsrmquota/IFsrmQuotaManager::GetRestrictiveQuota","fsrmquota/IFsrmQuotaManagerEx::GetRestrictiveQuota"]
old-location: fsrm\ifsrmquotamanager_getrestrictivequota.htm
tech.root: fsrm
ms.assetid: aa1ac69d-341e-49fd-893c-82ce3577c1f5
ms.date: 12/05/2018
ms.keywords: FsrmQuotaManager class [File Server Resource Manager],GetRestrictiveQuota method, GetRestrictiveQuota, GetRestrictiveQuota method [File Server Resource Manager], GetRestrictiveQuota method [File Server Resource Manager],FsrmQuotaManager class, GetRestrictiveQuota method [File Server Resource Manager],IFsrmQuotaManager interface, GetRestrictiveQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, IFsrmQuotaManager interface [File Server Resource Manager],GetRestrictiveQuota method, IFsrmQuotaManager.GetRestrictiveQuota, IFsrmQuotaManager::GetRestrictiveQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],GetRestrictiveQuota method, IFsrmQuotaManagerEx::GetRestrictiveQuota, fs.ifsrmquotamanager_getrestrictivequota, fsrm.ifsrmquotamanager_getrestrictivequota, fsrmquota/IFsrmQuotaManager::GetRestrictiveQuota, fsrmquota/IFsrmQuotaManagerEx::GetRestrictiveQuota
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
 - IFsrmQuotaManager::GetRestrictiveQuota
 - fsrmquota/IFsrmQuotaManager::GetRestrictiveQuota
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
 - IFsrmQuotaManager.GetRestrictiveQuota
 - IFsrmQuotaManagerEx.GetRestrictiveQuota
 - FsrmQuotaManager.GetRestrictiveQuota
---

# IFsrmQuotaManager::GetRestrictiveQuota


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the most restrictive quota for the specified path.

## -parameters

### -param path [in]

The local directory path. The string is limited to 260 characters.

### -param quota [out]

An <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a> interface to  the quota object.

## -returns

The method returns the following return values.

## -remarks

The most restrictive quota is the one with the lowest quota limit. If a quota higher in the directory tree 
    has a lower limit than the quota associated with the specified path, the former quota is returned. If two quotas 
    have the same limit, the quota that is higher in the directory tree is returned.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>