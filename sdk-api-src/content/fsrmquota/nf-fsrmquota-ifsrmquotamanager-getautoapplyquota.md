---
UID: NF:fsrmquota.IFsrmQuotaManager.GetAutoApplyQuota
title: IFsrmQuotaManager::GetAutoApplyQuota
author: windows-sdk-content
description: Retrieves the automatic quota for the specified directory.
old-location: fsrm\ifsrmquotamanager_getautoapplyquota.htm
tech.root: Fsrm
ms.assetid: e6a4645c-c323-4c28-a284-9ebb677aeebb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FsrmQuotaManager class [File Server Resource Manager],GetAutoApplyQuota method, GetAutoApplyQuota, GetAutoApplyQuota method [File Server Resource Manager], GetAutoApplyQuota method [File Server Resource Manager],FsrmQuotaManager class, GetAutoApplyQuota method [File Server Resource Manager],IFsrmQuotaManager interface, GetAutoApplyQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, IFsrmQuotaManager interface [File Server Resource Manager],GetAutoApplyQuota method, IFsrmQuotaManager.GetAutoApplyQuota, IFsrmQuotaManager::GetAutoApplyQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],GetAutoApplyQuota method, IFsrmQuotaManagerEx::GetAutoApplyQuota, fs.ifsrmquotamanager_getautoapplyquota, fsrm.ifsrmquotamanager_getautoapplyquota, fsrmquota/IFsrmQuotaManager::GetAutoApplyQuota, fsrmquota/IFsrmQuotaManagerEx::GetAutoApplyQuota
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmQuotaManager.GetAutoApplyQuota
 - IFsrmQuotaManagerEx.GetAutoApplyQuota
 - FsrmQuotaManager.GetAutoApplyQuota
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaManager::GetAutoApplyQuota


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the automatic quota for the specified directory.


## -parameters




### -param path [in]

The local directory path that contains the quota that you want to retrieve. The string is limited to 260 
      characters.


### -param quota [out]

An <a href="https://msdn.microsoft.com/3eb30caa-ce29-4898-b1a7-bd905031ca98">IFsrmAutoApplyQuota</a> interface to the quota 
      object.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

