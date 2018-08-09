---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.EnumTemplates
title: IFsrmQuotaTemplateManager::EnumTemplates
author: windows-sdk-content
description: Enumerates the quota templates on the server.
old-location: fsrm\ifsrmquotatemplatemanager_enumtemplates.htm
old-project: fsrm
ms.assetid: e5f5b94a-6b17-4379-9141-07ec70a830e9
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: EnumTemplates, EnumTemplates method [File Server Resource Manager], EnumTemplates method [File Server Resource Manager],FsrmQuotaTemplateManager class, EnumTemplates method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, FsrmQuotaTemplateManager class [File Server Resource Manager],EnumTemplates method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],EnumTemplates method, IFsrmQuotaTemplateManager.EnumTemplates, IFsrmQuotaTemplateManager::EnumTemplates, fs.ifsrmquotatemplatemanager_enumtemplates, fsrm.ifsrmquotatemplatemanager_enumtemplates, fsrmquota/IFsrmQuotaTemplateManager::EnumTemplates
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
 - IFsrmQuotaTemplateManager.EnumTemplates
 - FsrmQuotaTemplateManager.EnumTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaTemplateManager::EnumTemplates


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Enumerates the quota templates on the server.


## -parameters




### -param options [in]

Options to use when enumerating the quota templates. For possible values, see the 
      <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param quotaTemplates [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface 
      that contains a collection of quota templates.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="https://msdn.microsoft.com/de8ac383-f309-4320-bc77-c859ba27e1ca">IFsrmQuotaTemplate</a> interface.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/954dbbae-78b1-4530-af2d-a1fe0d23b83f">FsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/c6e782ff-b2e7-4bd6-bd9f-cc645c6ee5d6">IFsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

