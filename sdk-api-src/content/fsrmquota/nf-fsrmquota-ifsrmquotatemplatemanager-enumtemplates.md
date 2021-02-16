---
UID: NF:fsrmquota.IFsrmQuotaTemplateManager.EnumTemplates
title: IFsrmQuotaTemplateManager::EnumTemplates (fsrmquota.h)
description: Enumerates the quota templates on the server.
helpviewer_keywords: ["EnumTemplates","EnumTemplates method [File Server Resource Manager]","EnumTemplates method [File Server Resource Manager]","FsrmQuotaTemplateManager class","EnumTemplates method [File Server Resource Manager]","IFsrmQuotaTemplateManager interface","FsrmQuotaTemplateManager class [File Server Resource Manager]","EnumTemplates method","IFsrmQuotaTemplateManager interface [File Server Resource Manager]","EnumTemplates method","IFsrmQuotaTemplateManager.EnumTemplates","IFsrmQuotaTemplateManager::EnumTemplates","fs.ifsrmquotatemplatemanager_enumtemplates","fsrm.ifsrmquotatemplatemanager_enumtemplates","fsrmquota/IFsrmQuotaTemplateManager::EnumTemplates"]
old-location: fsrm\ifsrmquotatemplatemanager_enumtemplates.htm
tech.root: fsrm
ms.assetid: e5f5b94a-6b17-4379-9141-07ec70a830e9
ms.date: 12/05/2018
ms.keywords: EnumTemplates, EnumTemplates method [File Server Resource Manager], EnumTemplates method [File Server Resource Manager],FsrmQuotaTemplateManager class, EnumTemplates method [File Server Resource Manager],IFsrmQuotaTemplateManager interface, FsrmQuotaTemplateManager class [File Server Resource Manager],EnumTemplates method, IFsrmQuotaTemplateManager interface [File Server Resource Manager],EnumTemplates method, IFsrmQuotaTemplateManager.EnumTemplates, IFsrmQuotaTemplateManager::EnumTemplates, fs.ifsrmquotatemplatemanager_enumtemplates, fsrm.ifsrmquotatemplatemanager_enumtemplates, fsrmquota/IFsrmQuotaTemplateManager::EnumTemplates
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
 - IFsrmQuotaTemplateManager::EnumTemplates
 - fsrmquota/IFsrmQuotaTemplateManager::EnumTemplates
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
 - IFsrmQuotaTemplateManager.EnumTemplates
 - FsrmQuotaTemplateManager.EnumTemplates
---

# IFsrmQuotaTemplateManager::EnumTemplates


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Enumerates the quota templates on the server.

## -parameters

### -param options [in]

Options to use when enumerating the quota templates. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param quotaTemplates [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface 
      that contains a collection of quota templates.

Each item of the collection is a <b>VARIANT</b> of type 
       <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for 
       the <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplate">IFsrmQuotaTemplate</a> interface.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotatemplatemanager">FsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplatemanager">IFsrmQuotaTemplateManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>