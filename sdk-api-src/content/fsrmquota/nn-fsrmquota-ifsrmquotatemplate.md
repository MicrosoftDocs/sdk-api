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
f1_keywords:
- fsrmquota/IFsrmQuotaTemplate
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- SrmSvc.dll
api_name:
- IFsrmQuotaTemplate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmQuotaTemplate interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Used to configure templates from which new quota objects can be derived. Templates are 
    identified by a name and are used to simplify the configuration of directory quotas.

To create this interface, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-createtemplate">IFsrmQuotaTemplateManager::CreateTemplate</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-enumtemplates">IFsrmQuotaTemplateManager::EnumTemplates</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-gettemplate">IFsrmQuotaTemplateManager::GetTemplate</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplatemanager-importtemplates">IFsrmQuotaTemplateManager::ImportTemplates</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaTemplate</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>. <b>IFsrmQuotaTemplate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmQuotaTemplate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplate-commitandupdatederived">CommitAndUpdateDerived</a>
</td>
<td align="left" width="63%">
Saves the quota template and then applies any changes to the derived quota objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplate-copytemplate">CopyTemplate</a>
</td>
<td align="left" width="63%">
Copies the property values of the specified template to this template.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaTemplate</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplate-get_name">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves and sets the name of the quota template.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
 

 

