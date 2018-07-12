---
UID: NF:fsrmquota.IFsrmQuotaManager.Scan
title: IFsrmQuotaManager::Scan
author: windows-sdk-content
description: Starts a quota scan on the specified path.
old-location: fsrm\ifsrmquotamanager_scan.htm
old-project: fsrm
ms.assetid: 1581f4c7-a912-4214-9ad9-181ad5ebba7e
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: FsrmQuotaManager class [File Server Resource Manager],Scan method, IFsrmQuotaManager interface [File Server Resource Manager],Scan method, IFsrmQuotaManager.Scan, IFsrmQuotaManager::Scan, IFsrmQuotaManagerEx interface [File Server Resource Manager],Scan method, IFsrmQuotaManagerEx::Scan, Scan, Scan method [File Server Resource Manager], Scan method [File Server Resource Manager],FsrmQuotaManager class, Scan method [File Server Resource Manager],IFsrmQuotaManager interface, Scan method [File Server Resource Manager],IFsrmQuotaManagerEx interface, fs.ifsrmquotamanager_scan, fsrm.ifsrmquotamanager_scan, fsrmquota/IFsrmQuotaManager::Scan, fsrmquota/IFsrmQuotaManagerEx::Scan
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaManager::Scan


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

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




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

