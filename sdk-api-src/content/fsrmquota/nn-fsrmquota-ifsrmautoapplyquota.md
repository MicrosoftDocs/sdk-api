---
UID: NN:fsrmquota.IFsrmAutoApplyQuota
title: IFsrmAutoApplyQuota (fsrmquota.h)
description: Used to automatically add the quota to new and existing subdirectories of the directory on which the automatic quota is applied.
helpviewer_keywords: ["IFsrmAutoApplyQuota","IFsrmAutoApplyQuota interface [File Server Resource Manager]","IFsrmAutoApplyQuota interface [File Server Resource Manager]","described","fs.ifsrmautoapplyquota","fsrm.ifsrmautoapplyquota","fsrm/IFsrmAutoApplyQuota"]
old-location: fsrm\ifsrmautoapplyquota.htm
tech.root: fsrm
ms.assetid: 3eb30caa-ce29-4898-b1a7-bd905031ca98
ms.date: 12/05/2018
ms.keywords: IFsrmAutoApplyQuota, IFsrmAutoApplyQuota interface [File Server Resource Manager], IFsrmAutoApplyQuota interface [File Server Resource Manager],described, fs.ifsrmautoapplyquota, fsrm.ifsrmautoapplyquota, fsrm/IFsrmAutoApplyQuota
f1_keywords:
- fsrmquota/IFsrmAutoApplyQuota
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
- IFsrmAutoApplyQuota
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmAutoApplyQuota interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmautoquota">MSFT_FSRMAutoQuota</a> class.]

Used to automatically add the quota to new and existing subdirectories of the directory on which the 
    automatic quota is applied.

To create an automatic quota, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createautoapplyquota">IFsrmQuotaManager::CreateAutoApplyQuota</a> 
    method.

To retrieve this interface to an existing automatic quota, call one of the following methods:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumautoapplyquotas">IFsrmQuotaManager::EnumAutoApplyQuotas</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getautoapplyquota">IFsrmQuotaManager::GetAutoApplyQuota</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAutoApplyQuota</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>. <b>IFsrmAutoApplyQuota</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmAutoApplyQuota</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmautoapplyquota-commitandupdatederived">CommitAndUpdateDerived</a>
</td>
<td align="left" width="63%">
Saves the quota and then applies any changes to the derived quota objects.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAutoApplyQuota</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmautoapplyquota-get_excludefolders">ExcludeFolders</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets an array of subdirectories to exclude from the automatic quota.

</td>
</tr>
</table> 


## -remarks



To change the properties of an automatic quota, change the properties of the template from which the automatic 
    quota is derived. Then call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotatemplate-commitandupdatederived">IFsrmQuotaTemplate::CommitAndUpdateDerived</a> 
    method to update the properties of the automatic quotas and the quotas that derive from the automatic quota.

If any quota under the automatic quota's path was changed to a different template, it will not be changed to 
    the automatic quota's new settings until you call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmautoapplyquota-commitandupdatederived">IFsrmAutoApplyQuota::CommitAndUpdateDerived</a> 
    method.

Changes made to the automatic quota are reflected in new quotas only after the automatic quota is 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">committed</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createquota">IFsrmQuotaManager::CreateQuota</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmautoquota">MSFT_FSRMAutoQuota</a>
 

 

