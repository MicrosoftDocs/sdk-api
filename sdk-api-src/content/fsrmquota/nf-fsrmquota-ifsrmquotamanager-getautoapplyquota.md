---
UID: NF:fsrmquota.IFsrmQuotaManager.GetAutoApplyQuota
title: IFsrmQuotaManager::GetAutoApplyQuota (fsrmquota.h)
description: Retrieves the automatic quota for the specified directory.
helpviewer_keywords: ["FsrmQuotaManager class [File Server Resource Manager]","GetAutoApplyQuota method","GetAutoApplyQuota","GetAutoApplyQuota method [File Server Resource Manager]","GetAutoApplyQuota method [File Server Resource Manager]","FsrmQuotaManager class","GetAutoApplyQuota method [File Server Resource Manager]","IFsrmQuotaManager interface","GetAutoApplyQuota method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","IFsrmQuotaManager interface [File Server Resource Manager]","GetAutoApplyQuota method","IFsrmQuotaManager.GetAutoApplyQuota","IFsrmQuotaManager::GetAutoApplyQuota","IFsrmQuotaManagerEx interface [File Server Resource Manager]","GetAutoApplyQuota method","IFsrmQuotaManagerEx::GetAutoApplyQuota","fs.ifsrmquotamanager_getautoapplyquota","fsrm.ifsrmquotamanager_getautoapplyquota","fsrmquota/IFsrmQuotaManager::GetAutoApplyQuota","fsrmquota/IFsrmQuotaManagerEx::GetAutoApplyQuota"]
old-location: fsrm\ifsrmquotamanager_getautoapplyquota.htm
tech.root: fsrm
ms.assetid: e6a4645c-c323-4c28-a284-9ebb677aeebb
ms.date: 12/05/2018
ms.keywords: FsrmQuotaManager class [File Server Resource Manager],GetAutoApplyQuota method, GetAutoApplyQuota, GetAutoApplyQuota method [File Server Resource Manager], GetAutoApplyQuota method [File Server Resource Manager],FsrmQuotaManager class, GetAutoApplyQuota method [File Server Resource Manager],IFsrmQuotaManager interface, GetAutoApplyQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, IFsrmQuotaManager interface [File Server Resource Manager],GetAutoApplyQuota method, IFsrmQuotaManager.GetAutoApplyQuota, IFsrmQuotaManager::GetAutoApplyQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],GetAutoApplyQuota method, IFsrmQuotaManagerEx::GetAutoApplyQuota, fs.ifsrmquotamanager_getautoapplyquota, fsrm.ifsrmquotamanager_getautoapplyquota, fsrmquota/IFsrmQuotaManager::GetAutoApplyQuota, fsrmquota/IFsrmQuotaManagerEx::GetAutoApplyQuota
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
 - IFsrmQuotaManager::GetAutoApplyQuota
 - fsrmquota/IFsrmQuotaManager::GetAutoApplyQuota
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
 - IFsrmQuotaManager.GetAutoApplyQuota
 - IFsrmQuotaManagerEx.GetAutoApplyQuota
 - FsrmQuotaManager.GetAutoApplyQuota
---

# IFsrmQuotaManager::GetAutoApplyQuota


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the automatic quota for the specified directory.

## -parameters

### -param path [in]

The local directory path that contains the quota that you want to retrieve. The string is limited to 260 
      characters.

### -param quota [out]

An <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmautoapplyquota">IFsrmAutoApplyQuota</a> interface to the quota 
      object.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>