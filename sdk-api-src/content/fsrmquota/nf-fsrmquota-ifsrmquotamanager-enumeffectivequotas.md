---
UID: NF:fsrmquota.IFsrmQuotaManager.EnumEffectiveQuotas
title: IFsrmQuotaManager::EnumEffectiveQuotas
author: windows-sdk-content
description: Enumerates all the quotas that affect the specified path.
old-location: fsrm\ifsrmquotamanager_enumeffectivequotas.htm
tech.root: Fsrm
ms.assetid: abe5e73b-459a-4e2a-9917-91d3c85a15bc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumEffectiveQuotas, EnumEffectiveQuotas method [File Server Resource Manager], EnumEffectiveQuotas method [File Server Resource Manager],FsrmQuotaManager class, EnumEffectiveQuotas method [File Server Resource Manager],IFsrmQuotaManager interface, EnumEffectiveQuotas method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],EnumEffectiveQuotas method, IFsrmQuotaManager interface [File Server Resource Manager],EnumEffectiveQuotas method, IFsrmQuotaManager.EnumEffectiveQuotas, IFsrmQuotaManager::EnumEffectiveQuotas, IFsrmQuotaManagerEx interface [File Server Resource Manager],EnumEffectiveQuotas method, IFsrmQuotaManagerEx::EnumEffectiveQuotas, fs.ifsrmquotamanager_enumeffectivequotas, fsrm.ifsrmquotamanager_enumeffectivequotas, fsrmquota/IFsrmQuotaManager::EnumEffectiveQuotas, fsrmquota/IFsrmQuotaManagerEx::EnumEffectiveQuotas
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
 - IFsrmQuotaManager.EnumEffectiveQuotas
 - IFsrmQuotaManagerEx.EnumEffectiveQuotas
 - FsrmQuotaManager.EnumEffectiveQuotas
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmquota.h
: 
- IFsrmQuotaManager.EnumEffectiveQuotas
: 
---

# IFsrmQuotaManager::EnumEffectiveQuotas


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Enumerates all the quotas that affect the specified path.


## -parameters




### -param path [in]

A local directory path. The string is limited to 260 characters.


### -param options [in]

Options to use when enumerating the quotas. For possible values, see the 
      <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param quotas [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface 
       that contains a collection of the quotas configured at or above the specified path.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a> interface.

The collection is empty if the path does not contain quotas.


## -returns



The method returns the following return values.




## -remarks



Does not enumerate automatic quotas. To enumerate automatic quotas, call the 
    <a href="https://msdn.microsoft.com/6542bc4e-535f-4e6c-aaa8-ba6963490811">IFsrmQuotaManager::EnumAutoApplyQuotas</a> 
    method.

To enumerate all quotas, call the 
    <a href="https://msdn.microsoft.com/9977a519-4a6d-4b35-b973-4ef086e13e92">IFsrmQuotaManager::EnumQuotas</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

