---
UID: NF:fsrmquota.IFsrmQuotaManager.EnumQuotas
title: IFsrmQuotaManager::EnumQuotas (fsrmquota.h)
author: windows-sdk-content
description: Enumerates the quotas for the specified directory and any quotas associated with its subdirectories (recursively).
old-location: fsrm\ifsrmquotamanager_enumquotas.htm
tech.root: fsrm
ms.assetid: 9977a519-4a6d-4b35-b973-4ef086e13e92
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumQuotas, EnumQuotas method [File Server Resource Manager], EnumQuotas method [File Server Resource Manager],FsrmQuotaManager class, EnumQuotas method [File Server Resource Manager],IFsrmQuotaManager interface, EnumQuotas method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],EnumQuotas method, IFsrmQuotaManager interface [File Server Resource Manager],EnumQuotas method, IFsrmQuotaManager.EnumQuotas, IFsrmQuotaManager::EnumQuotas, IFsrmQuotaManagerEx interface [File Server Resource Manager],EnumQuotas method, IFsrmQuotaManagerEx::EnumQuotas, fs.ifsrmquotamanager_enumquotas, fsrm.ifsrmquotamanager_enumquotas, fsrmquota/IFsrmQuotaManager::EnumQuotas, fsrmquota/IFsrmQuotaManagerEx::EnumQuotas
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
 - IFsrmQuotaManager.EnumQuotas
 - IFsrmQuotaManagerEx.EnumQuotas
 - FsrmQuotaManager.EnumQuotas
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaManager::EnumQuotas


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Enumerates the quotas for the specified directory and any quotas associated with its subdirectories 
    (recursively).


## -parameters




### -param path [in]

The local directory path that is associated with the quota that you want to enumerate. The string is limited 
       to 260 characters.

If the path ends with "\*", retrieve all quotas associated with the immediate subdirectories 
       of the path (does not include the quota associated with the path).

If the path ends with "\...", retrieve the quota for the path and all quotas associated with 
       the immediate subdirectories of the path (recursively).

If the path does not end in "\*" or "\...", retrieve the quota for the path 
       only.

If path is null or empty, the method returns all quotas.


### -param options [in]

Options to use when enumerating the quotas. For possible values, see the 
      <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param quotas [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface 
       that contains a collection of the quotas.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a> interface.

The collection is empty if the path does not contain quotas.


## -returns



The method returns the following return values.




## -remarks



To enumerate quotas that apply automatically to the path's subdirectories, call the 
    <a href="https://msdn.microsoft.com/6542bc4e-535f-4e6c-aaa8-ba6963490811">IFsrmQuotaManager::EnumAutoApplyQuotas</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

