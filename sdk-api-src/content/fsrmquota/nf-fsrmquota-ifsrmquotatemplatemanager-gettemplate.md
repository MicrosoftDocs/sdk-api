---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.GetTemplate
title: IFsrmQuotaTemplateManager::GetTemplate (fsrmquota.h)
author: windows-sdk-content
description: Retrieves the specified quota template.
old-location: fsrm\ifsrmquotatemplatemanager_gettemplate.htm
tech.root: fsrm
ms.assetid: 2877c453-aad7-42ea-a66d-b49ab1f8f854
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FsrmQuotaTemplateManager class [File Server Resource Manager],GetTemplate method, GetTemplate, GetTemplate method [File Server Resource Manager], GetTemplate method [File Server Resource Manager],FsrmQuotaTemplateManager class, GetTemplate method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, IFsrmQuotaTemplateManager interface [File Server Resource Manager],GetTemplate method, IFsrmQuotaTemplateManager.GetTemplate, IFsrmQuotaTemplateManager::GetTemplate, fs.ifsrmquotatemplatemanager_gettemplate, fsrm.ifsrmquotatemplatemanager_gettemplate, fsrmquota/IFsrmQuotaTemplateManager::GetTemplate
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
 - IFsrmQuotaTemplateManager.GetTemplate
 - FsrmQuotaTemplateManager.GetTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmQuotaTemplateManager::GetTemplate


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the specified quota template.


## -parameters




### -param name [in]

The name of the quota template to retrieve. The string is limited to 4,000 characters.


### -param quotaTemplate [out]

An <a href="https://msdn.microsoft.com/de8ac383-f309-4320-bc77-c859ba27e1ca">IFsrmQuotaTemplate</a> interface to the retrieved 
      template object.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/954dbbae-78b1-4530-af2d-a1fe0d23b83f">FsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/c6e782ff-b2e7-4bd6-bd9f-cc645c6ee5d6">IFsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

