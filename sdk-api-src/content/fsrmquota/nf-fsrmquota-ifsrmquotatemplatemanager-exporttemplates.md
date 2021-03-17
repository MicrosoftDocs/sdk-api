---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.ExportTemplates
title: IFsrmQuotaTemplateManager::ExportTemplates (fsrmquota.h)
description: Exports the quota templates as an XML string.
helpviewer_keywords: ["ExportTemplates","ExportTemplates method [File Server Resource Manager]","ExportTemplates method [File Server Resource Manager]","FsrmQuotaTemplateManager class","ExportTemplates method [File Server Resource Manager]","IFsrmQuotaTemplateManager interface","FsrmQuotaTemplateManager class [File Server Resource Manager]","ExportTemplates method","IFsrmQuotaTemplateManager interface [File Server Resource Manager]","ExportTemplates method","IFsrmQuotaTemplateManager.ExportTemplates","IFsrmQuotaTemplateManager::ExportTemplates","fs.ifsrmquotatemplatemanager_exporttemplates","fsrm.ifsrmquotatemplatemanager_exporttemplates","fsrmquota/IFsrmQuotaTemplateManager::ExportTemplates"]
old-location: fsrm\ifsrmquotatemplatemanager_exporttemplates.htm
tech.root: fsrm
ms.assetid: 36ba071b-4db2-42fb-90a8-838c45dfdd16
ms.date: 12/05/2018
ms.keywords: ExportTemplates, ExportTemplates method [File Server Resource Manager], ExportTemplates method [File Server Resource Manager],FsrmQuotaTemplateManager class, ExportTemplates method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, FsrmQuotaTemplateManager class [File Server Resource Manager],ExportTemplates method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],ExportTemplates method, IFsrmQuotaTemplateManager.ExportTemplates, IFsrmQuotaTemplateManager::ExportTemplates, fs.ifsrmquotatemplatemanager_exporttemplates, fsrm.ifsrmquotatemplatemanager_exporttemplates, fsrmquota/IFsrmQuotaTemplateManager::ExportTemplates
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
 - IFsrmQuotaTemplateManager::ExportTemplates
 - fsrmquota/IFsrmQuotaTemplateManager::ExportTemplates
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
 - IFsrmQuotaTemplateManager.ExportTemplates
 - FsrmQuotaTemplateManager.ExportTemplates
---

# IFsrmQuotaTemplateManager::ExportTemplates


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

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
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-importtemplates">IFsrmQuotaTemplateManager::ImportTemplates</a> 
    method to import the templates.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotatemplatemanager">FsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplatemanager">IFsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>