---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.CreateTemplate
title: IFsrmQuotaTemplateManager::CreateTemplate (fsrmquota.h)
author: windows-sdk-content
description: Creates a quota template object.
old-location: fsrm\ifsrmquotatemplatemanager_createtemplate.htm
tech.root: fsrm
ms.assetid: d8dbc0fb-de02-4491-94f5-e845a2338251
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateTemplate, CreateTemplate method [File Server Resource Manager], CreateTemplate method [File Server Resource Manager],FsrmQuotaTemplateManager class, CreateTemplate method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, FsrmQuotaTemplateManager class [File Server Resource Manager],CreateTemplate method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],CreateTemplate method, IFsrmQuotaTemplateManager.CreateTemplate, IFsrmQuotaTemplateManager::CreateTemplate, fs.ifsrmquotatemplatemanager_createtemplate, fsrm.ifsrmquotatemplatemanager_createtemplate, fsrmquota/IFsrmQuotaTemplateManager::CreateTemplate
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
 - IFsrmQuotaTemplateManager.CreateTemplate
 - FsrmQuotaTemplateManager.CreateTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaTemplateManager::CreateTemplate


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Creates a quota template object.


## -parameters




### -param quotaTemplate [out]

An <a href="https://msdn.microsoft.com/de8ac383-f309-4320-bc77-c859ba27e1ca">IFsrmQuotaTemplate</a> interface to the newly 
      create template. To add the template to FSRM, call 
      <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmQuotaTemplate::Commit</a> method.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/954dbbae-78b1-4530-af2d-a1fe0d23b83f">FsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/c6e782ff-b2e7-4bd6-bd9f-cc645c6ee5d6">IFsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

