---
UID: NN:fsrmquota.IFsrmQuota
title: IFsrmQuota (fsrmquota.h)
description: Used to define a quota for a specified directory and to retrieve use statistics.helpviewer_keywords: ["IFsrmQuota","IFsrmQuota interface [File Server Resource Manager]","IFsrmQuota interface [File Server Resource Manager]","described","fs.ifsrmquota","fsrm.ifsrmquota","fsrm/IFsrmQuota"]
old-location: fsrm\ifsrmquota.htm
tech.root: fsrm
ms.assetid: 91ced22a-01b9-4fcf-b61a-c99e6f0286f3
ms.date: 12/05/2018
ms.keywords: IFsrmQuota, IFsrmQuota interface [File Server Resource Manager], IFsrmQuota interface [File Server Resource Manager],described, fs.ifsrmquota, fsrm.ifsrmquota, fsrm/IFsrmQuota
f1_keywords:
- fsrmquota/IFsrmQuota
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
- IFsrmQuota
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmQuota interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Used to define a quota for a specified directory and to retrieve use statistics. 

To create this interface, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createquota">IFsrmQuotaManager::CreateQuota</a> method.

The following methods return this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumeffectivequotas">IFsrmQuotaManager::EnumEffectiveQuotas</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumquotas">IFsrmQuotaManager::EnumQuotas</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getquota">IFsrmQuotaManager::GetQuota</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getrestrictivequota">IFsrmQuotaManager::GetRestrictiveQuota</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuota</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>. <b>IFsrmQuota</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmQuota</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-refreshusageproperties">RefreshUsageProperties</a>
</td>
<td align="left" width="63%">
Refreshes this object's quota usage information from the current information in FSRM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-resetpeakusage">ResetPeakUsage</a>
</td>
<td align="left" width="63%">
Resets the peak usage of this quota to the current usage.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuota</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-get_quotapeakusage">QuotaPeakUsage</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the highest amount of disk space usage charged to this quota.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-get_quotapeakusagetime">QuotaPeakUsageTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the date and time that the quota's peak usage occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-get_quotaused">QuotaUsed</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the current amount of disk space usage charged to this quota.

</td>
</tr>
</table> 


## -remarks



A quota limits the amount of data that the system or any user can store in a directory.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
 

 

