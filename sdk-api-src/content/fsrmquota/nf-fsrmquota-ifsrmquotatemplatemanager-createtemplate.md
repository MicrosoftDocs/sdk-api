---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.CreateTemplate
title: IFsrmQuotaTemplateManager::CreateTemplate (fsrmquota.h)
description: Creates a quota template object.
helpviewer_keywords: ["CreateTemplate","CreateTemplate method [File Server Resource Manager]","CreateTemplate method [File Server Resource Manager]","FsrmQuotaTemplateManager class","CreateTemplate method [File Server Resource Manager]","IFsrmQuotaTemplateManager interface","FsrmQuotaTemplateManager class [File Server Resource Manager]","CreateTemplate method","IFsrmQuotaTemplateManager interface [File Server Resource Manager]","CreateTemplate method","IFsrmQuotaTemplateManager.CreateTemplate","IFsrmQuotaTemplateManager::CreateTemplate","fs.ifsrmquotatemplatemanager_createtemplate","fsrm.ifsrmquotatemplatemanager_createtemplate","fsrmquota/IFsrmQuotaTemplateManager::CreateTemplate"]
old-location: fsrm\ifsrmquotatemplatemanager_createtemplate.htm
tech.root: fsrm
ms.assetid: d8dbc0fb-de02-4491-94f5-e845a2338251
ms.date: 12/05/2018
ms.keywords: CreateTemplate, CreateTemplate method [File Server Resource Manager], CreateTemplate method [File Server Resource Manager],FsrmQuotaTemplateManager class, CreateTemplate method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, FsrmQuotaTemplateManager class [File Server Resource Manager],CreateTemplate method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],CreateTemplate method, IFsrmQuotaTemplateManager.CreateTemplate, IFsrmQuotaTemplateManager::CreateTemplate, fs.ifsrmquotatemplatemanager_createtemplate, fsrm.ifsrmquotatemplatemanager_createtemplate, fsrmquota/IFsrmQuotaTemplateManager::CreateTemplate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmQuotaTemplateManager::CreateTemplate
 - fsrmquota/IFsrmQuotaTemplateManager::CreateTemplate
dev_langs:
 - c++
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
---

# IFsrmQuotaTemplateManager::CreateTemplate


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Creates a quota template object.

## -parameters

### -param quotaTemplate [out]

An <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplate">IFsrmQuotaTemplate</a> interface to the newly 
      create template. To add the template to FSRM, call 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmQuotaTemplate::Commit</a> method.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotatemplatemanager">FsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplatemanager">IFsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>