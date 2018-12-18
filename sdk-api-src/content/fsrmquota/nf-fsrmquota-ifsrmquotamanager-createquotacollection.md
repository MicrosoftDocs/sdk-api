---
UID: NF:fsrmquota.IFsrmQuotaManager.CreateQuotaCollection
title: IFsrmQuotaManager::CreateQuotaCollection
author: windows-sdk-content
description: Creates an empty collection to which you can add quotas.
old-location: fsrm\ifsrmquotamanager_createquotacollection.htm
tech.root: fsrm
ms.assetid: 88656cb9-1e72-4f82-ac09-fbb3c8a36afc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateQuotaCollection, CreateQuotaCollection method [File Server Resource Manager], CreateQuotaCollection method [File Server Resource Manager],FsrmQuotaManager class, CreateQuotaCollection method [File Server Resource Manager],IFsrmQuotaManager interface, CreateQuotaCollection method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],CreateQuotaCollection method, IFsrmQuotaManager interface [File Server Resource Manager],CreateQuotaCollection method, IFsrmQuotaManager.CreateQuotaCollection, IFsrmQuotaManager::CreateQuotaCollection, IFsrmQuotaManagerEx interface [File Server Resource Manager],CreateQuotaCollection method, IFsrmQuotaManagerEx::CreateQuotaCollection, fs.ifsrmquotamanager_createquotacollection, fsrm.ifsrmquotamanager_createquotacollection, fsrmquota/IFsrmQuotaManager::CreateQuotaCollection, fsrmquota/IFsrmQuotaManagerEx::CreateQuotaCollection
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
 - IFsrmQuotaManager.CreateQuotaCollection
 - IFsrmQuotaManagerEx.CreateQuotaCollection
 - FsrmQuotaManager.CreateQuotaCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaManager::CreateQuotaCollection


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Creates an empty collection to which you can add quotas.


## -parameters




### -param collection [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface 
      to the newly created collection. To add an object to the collection, call the 
      <a href="https://msdn.microsoft.com/916f01de-c87c-450c-859a-c349a165f91d">IFsrmMutableCollection::Add</a> method.


## -returns



The method returns the following return values.




## -remarks



Using the collection to add more than one quota provides better performance than adding individual quotas. 
    After adding the quotas to the collection, call the 
    <a href="https://msdn.microsoft.com/844cb2a5-8526-434b-af22-b1bf856ed6af">IFsrmCommittableCollection::Commit</a> 
    method.




## -see-also




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

