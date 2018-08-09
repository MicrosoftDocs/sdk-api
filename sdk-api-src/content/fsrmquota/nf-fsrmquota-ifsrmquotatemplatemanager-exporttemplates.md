---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.ExportTemplates
title: IFsrmQuotaTemplateManager::ExportTemplates
author: windows-sdk-content
description: Exports the quota templates as an XML string.
old-location: fsrm\ifsrmquotatemplatemanager_exporttemplates.htm
old-project: fsrm
ms.assetid: 36ba071b-4db2-42fb-90a8-838c45dfdd16
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: ExportTemplates, ExportTemplates method [File Server Resource Manager], ExportTemplates method [File Server Resource Manager],FsrmQuotaTemplateManager class, ExportTemplates method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, FsrmQuotaTemplateManager class [File Server Resource Manager],ExportTemplates method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],ExportTemplates method, IFsrmQuotaTemplateManager.ExportTemplates, IFsrmQuotaTemplateManager::ExportTemplates, fs.ifsrmquotatemplatemanager_exporttemplates, fsrm.ifsrmquotatemplatemanager_exporttemplates, fsrmquota/IFsrmQuotaTemplateManager::ExportTemplates
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
 - IFsrmQuotaTemplateManager.ExportTemplates
 - FsrmQuotaTemplateManager.ExportTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaTemplateManager::ExportTemplates


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Exports the quota templates as an XML string.


## -parameters




### -param quotaTemplateNamesArray [in]

A variant that contains the names of the quota templates to export. If 
      <b>NULL</b>, the method exports all quotas.


### -param serializedQuotaTemplates [out]

The specified templates in XML format.


## -returns



The method returns the following return values.




## -remarks



Typically, you use this method to save the templates to a file. You can then copy the file to another computer 
    and call the 
    <a href="https://msdn.microsoft.com/f530d7fc-8b41-4a5e-a10a-b9211c7fe2bb">IFsrmQuotaTemplateManager::ImportTemplates</a> 
    method to import the templates.




## -see-also




<a href="https://msdn.microsoft.com/954dbbae-78b1-4530-af2d-a1fe0d23b83f">FsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/c6e782ff-b2e7-4bd6-bd9f-cc645c6ee5d6">IFsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

