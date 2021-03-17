---
UID: NF:fsrmquota.IFsrmQuotaManager.GetQuota
title: IFsrmQuotaManager::GetQuota (fsrmquota.h)
description: Retrieves the quota for the specified directory.
helpviewer_keywords: ["FsrmQuotaManager class [File Server Resource Manager]","GetQuota method","GetQuota","GetQuota method [File Server Resource Manager]","GetQuota method [File Server Resource Manager]","FsrmQuotaManager class","GetQuota method [File Server Resource Manager]","IFsrmQuotaManager interface","GetQuota method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","IFsrmQuotaManager interface [File Server Resource Manager]","GetQuota method","IFsrmQuotaManager.GetQuota","IFsrmQuotaManager::GetQuota","IFsrmQuotaManagerEx interface [File Server Resource Manager]","GetQuota method","IFsrmQuotaManagerEx::GetQuota","fs.ifsrmquotamanager_getquota","fsrm.ifsrmquotamanager_getquota","fsrmquota/IFsrmQuotaManager::GetQuota","fsrmquota/IFsrmQuotaManagerEx::GetQuota"]
old-location: fsrm\ifsrmquotamanager_getquota.htm
tech.root: fsrm
ms.assetid: 1c595714-20c9-4ca5-96a2-64b7a7c6f84e
ms.date: 12/05/2018
ms.keywords: FsrmQuotaManager class [File Server Resource Manager],GetQuota method, GetQuota, GetQuota method [File Server Resource Manager], GetQuota method [File Server Resource Manager],FsrmQuotaManager class, GetQuota method [File Server Resource Manager],IFsrmQuotaManager interface, GetQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, IFsrmQuotaManager interface [File Server Resource Manager],GetQuota method, IFsrmQuotaManager.GetQuota, IFsrmQuotaManager::GetQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],GetQuota method, IFsrmQuotaManagerEx::GetQuota, fs.ifsrmquotamanager_getquota, fsrm.ifsrmquotamanager_getquota, fsrmquota/IFsrmQuotaManager::GetQuota, fsrmquota/IFsrmQuotaManagerEx::GetQuota
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
 - IFsrmQuotaManager::GetQuota
 - fsrmquota/IFsrmQuotaManager::GetQuota
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
 - IFsrmQuotaManager.GetQuota
 - IFsrmQuotaManagerEx.GetQuota
 - FsrmQuotaManager.GetQuota
---

# IFsrmQuotaManager::GetQuota


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the quota for the specified directory.

## -parameters

### -param path [in]

The local directory path that contains the quota that you want to retrieve. The string is limited to 260 
      characters.

### -param quota [out]

An <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a> interface to the quota object.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>