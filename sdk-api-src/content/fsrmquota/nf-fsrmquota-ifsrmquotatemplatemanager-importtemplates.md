---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.ImportTemplates
title: IFsrmQuotaTemplateManager::ImportTemplates
author: windows-sdk-content
description: Imports the specified quota templates from an XML string.
old-location: fsrm\ifsrmquotatemplatemanager_importtemplates.htm
old-project: Fsrm
ms.assetid: f530d7fc-8b41-4a5e-a10a-b9211c7fe2bb
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FsrmQuotaTemplateManager class [File Server Resource Manager],ImportTemplates method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],ImportTemplates method, IFsrmQuotaTemplateManager.ImportTemplates, IFsrmQuotaTemplateManager::ImportTemplates, ImportTemplates, ImportTemplates method [File Server Resource Manager], ImportTemplates method [File Server Resource Manager],FsrmQuotaTemplateManager class, ImportTemplates method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, fs.ifsrmquotatemplatemanager_importtemplates, fsrm.ifsrmquotatemplatemanager_importtemplates, fsrmquota/IFsrmQuotaTemplateManager::ImportTemplates
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
 - IFsrmQuotaTemplateManager.ImportTemplates
 - FsrmQuotaTemplateManager.ImportTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaTemplateManager::ImportTemplates


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Imports the specified quota templates from an XML string.


## -parameters




### -param serializedQuotaTemplates [in]

An XML string that represents one or more quota templates.


### -param quotaTemplateNamesArray [in]

A variant that contains the names of the templates to import. If <b>NULL</b>, the method 
      imports all templates.


### -param quotaTemplates [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface 
       that contains a collection of quota templates.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="https://msdn.microsoft.com/0349a772-9862-4131-b3be-96eec8e41b01">IFsrmQuotaTemplateImported</a> interface.

To add the templates to FSRM, call the 
       <a href="https://msdn.microsoft.com/844cb2a5-8526-434b-af22-b1bf856ed6af">IFsrmCommittableCollection::Commit</a> 
       method. To add the templates to FSRM and propagate the changes to objects that were derived from the template, 
       call the 
       <a href="https://msdn.microsoft.com/6b50a93f-f6f0-4ab4-a4a3-3995b721c5d7">IFsrmFileScreenTemplateImported::CommitAndUpdateDerived</a> 
       method on each item in the collection.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/954dbbae-78b1-4530-af2d-a1fe0d23b83f">FsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/c6e782ff-b2e7-4bd6-bd9f-cc645c6ee5d6">IFsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

