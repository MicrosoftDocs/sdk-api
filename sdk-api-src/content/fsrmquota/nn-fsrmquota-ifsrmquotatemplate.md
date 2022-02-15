---
UID: NN:fsrmquota.IFsrmQuotaTemplate
title: IFsrmQuotaTemplate (fsrmquota.h)
description: Used to configure templates from which new quota objects can be derived.
helpviewer_keywords: ["IFsrmQuotaTemplate","IFsrmQuotaTemplate interface [File Server Resource Manager]","IFsrmQuotaTemplate interface [File Server Resource Manager]","described","fs.ifsrmquotatemplate","fsrm.ifsrmquotatemplate","fsrm/IFsrmQuotaTemplate"]
old-location: fsrm\ifsrmquotatemplate.htm
tech.root: fsrm
ms.assetid: de8ac383-f309-4320-bc77-c859ba27e1ca
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaTemplate, IFsrmQuotaTemplate interface [File Server Resource Manager], IFsrmQuotaTemplate interface [File Server Resource Manager],described, fs.ifsrmquotatemplate, fsrm.ifsrmquotatemplate, fsrm/IFsrmQuotaTemplate
req.header: fsrmquota.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmQuotaTemplate
 - fsrmquota/IFsrmQuotaTemplate
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
 - IFsrmQuotaTemplate
---

# IFsrmQuotaTemplate interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Used to configure templates from which new quota objects can be derived. Templates are 
    identified by a name and are used to simplify the configuration of directory quotas.

To create this interface, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-createtemplate">IFsrmQuotaTemplateManager::CreateTemplate</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-enumtemplates">IFsrmQuotaTemplateManager::EnumTemplates</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-gettemplate">IFsrmQuotaTemplateManager::GetTemplate</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-importtemplates">IFsrmQuotaTemplateManager::ImportTemplates</a>
</li>
</ul>

## -inheritance

The <b>IFsrmQuotaTemplate</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>. <b>IFsrmQuotaTemplate</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
