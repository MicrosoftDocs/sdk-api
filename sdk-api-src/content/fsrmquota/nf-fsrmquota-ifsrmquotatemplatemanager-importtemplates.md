---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.ImportTemplates
title: IFsrmQuotaTemplateManager::ImportTemplates (fsrmquota.h)
description: Imports the specified quota templates from an XML string.
helpviewer_keywords: ["FsrmQuotaTemplateManager class [File Server Resource Manager]","ImportTemplates method","IFsrmQuotaTemplateManager interface [File Server Resource Manager]","ImportTemplates method","IFsrmQuotaTemplateManager.ImportTemplates","IFsrmQuotaTemplateManager::ImportTemplates","ImportTemplates","ImportTemplates method [File Server Resource Manager]","ImportTemplates method [File Server Resource Manager]","FsrmQuotaTemplateManager class","ImportTemplates method [File Server Resource Manager]","IFsrmQuotaTemplateManager interface","fs.ifsrmquotatemplatemanager_importtemplates","fsrm.ifsrmquotatemplatemanager_importtemplates","fsrmquota/IFsrmQuotaTemplateManager::ImportTemplates"]
old-location: fsrm\ifsrmquotatemplatemanager_importtemplates.htm
tech.root: fsrm
ms.assetid: f530d7fc-8b41-4a5e-a10a-b9211c7fe2bb
ms.date: 12/05/2018
ms.keywords: FsrmQuotaTemplateManager class [File Server Resource Manager],ImportTemplates method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],ImportTemplates method, IFsrmQuotaTemplateManager.ImportTemplates, IFsrmQuotaTemplateManager::ImportTemplates, ImportTemplates, ImportTemplates method [File Server Resource Manager], ImportTemplates method [File Server Resource Manager],FsrmQuotaTemplateManager class, ImportTemplates method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, fs.ifsrmquotatemplatemanager_importtemplates, fsrm.ifsrmquotatemplatemanager_importtemplates, fsrmquota/IFsrmQuotaTemplateManager::ImportTemplates
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
 - IFsrmQuotaTemplateManager::ImportTemplates
 - fsrmquota/IFsrmQuotaTemplateManager::ImportTemplates
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
 - IFsrmQuotaTemplateManager.ImportTemplates
 - FsrmQuotaTemplateManager.ImportTemplates
---

# IFsrmQuotaTemplateManager::ImportTemplates


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Imports the specified quota templates from an XML string.

## -parameters

### -param serializedQuotaTemplates [in]

An XML string that represents one or more quota templates.

### -param quotaTemplateNamesArray [in]

A variant that contains the names of the templates to import. If <b>NULL</b>, the method 
      imports all templates.

### -param quotaTemplates [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
       that contains a collection of quota templates.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplateimported">IFsrmQuotaTemplateImported</a> interface.

To add the templates to FSRM, call the 
       <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a> 
       method. To add the templates to FSRM and propagate the changes to objects that were derived from the template, 
       call the 
       <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-commitandupdatederived">IFsrmFileScreenTemplateImported::CommitAndUpdateDerived</a> 
       method on each item in the collection.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotatemplatemanager">FsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplatemanager">IFsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>