---
UID: NF:fsrmquota.IFsrmQuotaManager.GetRestrictiveQuota
title: IFsrmQuotaManager::GetRestrictiveQuota (fsrmquota.h)
author: windows-sdk-content
description: Retrieves the most restrictive quota for the specified path.
old-location: fsrm\ifsrmquotamanager_getrestrictivequota.htm
tech.root: fsrm
ms.assetid: aa1ac69d-341e-49fd-893c-82ce3577c1f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FsrmQuotaManager class [File Server Resource Manager],GetRestrictiveQuota method, GetRestrictiveQuota, GetRestrictiveQuota method [File Server Resource Manager], GetRestrictiveQuota method [File Server Resource Manager],FsrmQuotaManager class, GetRestrictiveQuota method [File Server Resource Manager],IFsrmQuotaManager interface, GetRestrictiveQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, IFsrmQuotaManager interface [File Server Resource Manager],GetRestrictiveQuota method, IFsrmQuotaManager.GetRestrictiveQuota, IFsrmQuotaManager::GetRestrictiveQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],GetRestrictiveQuota method, IFsrmQuotaManagerEx::GetRestrictiveQuota, fs.ifsrmquotamanager_getrestrictivequota, fsrm.ifsrmquotamanager_getrestrictivequota, fsrmquota/IFsrmQuotaManager::GetRestrictiveQuota, fsrmquota/IFsrmQuotaManagerEx::GetRestrictiveQuota
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
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaManager::GetRestrictiveQuota


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the most restrictive quota for the specified path.


## -parameters




### -param path [in]

The local directory path. The string is limited to 260 characters.


### -param quota [out]

An <a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a> interface to  the quota object.


## -returns



The method returns the following return values.




## -remarks



The most restrictive quota is the one with the lowest quota limit. If a quota higher in the directory tree 
    has a lower limit than the quota associated with the specified path, the former quota is returned. If two quotas 
    have the same limit, the quota that is higher in the directory tree is returned.




## -see-also




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

