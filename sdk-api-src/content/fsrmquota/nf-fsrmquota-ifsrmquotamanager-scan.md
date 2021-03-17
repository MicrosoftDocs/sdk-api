---
UID: NF:fsrmquota.IFsrmQuotaManager.Scan
title: IFsrmQuotaManager::Scan (fsrmquota.h)
description: Starts a quota scan on the specified path.
helpviewer_keywords: ["FsrmQuotaManager class [File Server Resource Manager]","Scan method","IFsrmQuotaManager interface [File Server Resource Manager]","Scan method","IFsrmQuotaManager.Scan","IFsrmQuotaManager::Scan","IFsrmQuotaManagerEx interface [File Server Resource Manager]","Scan method","IFsrmQuotaManagerEx::Scan","Scan","Scan method [File Server Resource Manager]","Scan method [File Server Resource Manager]","FsrmQuotaManager class","Scan method [File Server Resource Manager]","IFsrmQuotaManager interface","Scan method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","fs.ifsrmquotamanager_scan","fsrm.ifsrmquotamanager_scan","fsrmquota/IFsrmQuotaManager::Scan","fsrmquota/IFsrmQuotaManagerEx::Scan"]
old-location: fsrm\ifsrmquotamanager_scan.htm
tech.root: fsrm
ms.assetid: 1581f4c7-a912-4214-9ad9-181ad5ebba7e
ms.date: 12/05/2018
ms.keywords: FsrmQuotaManager class [File Server Resource Manager],Scan method, IFsrmQuotaManager interface [File Server Resource Manager],Scan method, IFsrmQuotaManager.Scan, IFsrmQuotaManager::Scan, IFsrmQuotaManagerEx interface [File Server Resource Manager],Scan method, IFsrmQuotaManagerEx::Scan, Scan, Scan method [File Server Resource Manager], Scan method [File Server Resource Manager],FsrmQuotaManager class, Scan method [File Server Resource Manager],IFsrmQuotaManager interface, Scan method [File Server Resource Manager],IFsrmQuotaManagerEx interface, fs.ifsrmquotamanager_scan, fsrm.ifsrmquotamanager_scan, fsrmquota/IFsrmQuotaManager::Scan, fsrmquota/IFsrmQuotaManagerEx::Scan
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
 - IFsrmQuotaManager::Scan
 - fsrmquota/IFsrmQuotaManager::Scan
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
 - IFsrmQuotaManager.Scan
 - IFsrmQuotaManagerEx.Scan
 - FsrmQuotaManager.Scan
---

# IFsrmQuotaManager::Scan


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Starts a quota scan on the specified path.

## -parameters

### -param strPath [in]

The local directory path to scan.

## -returns

The method returns the following return values.

## -remarks

Although quota usage is monitored on an ongoing basis, there may be some instances in which the quota usage 
    may be out of sync with the actual usage, in which case you can call this method to refresh the quota usage. For 
    example, if an administrator disables a quota (to investigate or troubleshoot an issue) and later enables it, then 
    this method should be called to perform a manual scan.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>