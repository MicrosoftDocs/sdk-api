---
UID: NN:fsrmquota.IFsrmQuota
title: IFsrmQuota
author: windows-driver-content
description: Used to define a quota for a specified directory and to retrieve use statistics.
old-location: fsrm\ifsrmquota.htm
old-project: Fsrm
ms.assetid: 91ced22a-01b9-4fcf-b61a-c99e6f0286f3
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFsrmQuota, IFsrmQuota interface [File Server Resource Manager], IFsrmQuota interface [File Server Resource Manager],described, fs.ifsrmquota, fsrm.ifsrmquota, fsrm/IFsrmQuota
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmQuota
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuota interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Used to define a quota for a specified directory and to retrieve use statistics. 

To create this interface, call the 
    <a href="https://msdn.microsoft.com/09f0b952-e24f-4388-8e82-6b34145f9ad4">IFsrmQuotaManager::CreateQuota</a> method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/abe5e73b-459a-4e2a-9917-91d3c85a15bc">IFsrmQuotaManager::EnumEffectiveQuotas</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9977a519-4a6d-4b35-b973-4ef086e13e92">IFsrmQuotaManager::EnumQuotas</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1c595714-20c9-4ca5-96a2-64b7a7c6f84e">IFsrmQuotaManager::GetQuota</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aa1ac69d-341e-49fd-893c-82ce3577c1f5">IFsrmQuotaManager::GetRestrictiveQuota</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuota</b> interface inherits from <a href="https://msdn.microsoft.com/80c01faf-717e-4375-8772-c61f04a7d7f3">IFsrmQuotaObject</a>. <b>IFsrmQuota</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1aa20d1a-4259-4ae0-9717-957f7b8b984e">RefreshUsageProperties</a>
</td>
<td align="left" width="63%">
Refreshes this object's quota usage information from the current information in FSRM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c2b18a9-912a-49cc-bf4f-07f172a328b1">ResetPeakUsage</a>
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

<a href="https://msdn.microsoft.com/86e2f8a1-766e-494d-9b99-c55e51d8509c">QuotaPeakUsage</a>


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

<a href="https://msdn.microsoft.com/08b7c438-6bcf-4323-ac27-7e3c79c062da">QuotaPeakUsageTime</a>


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

<a href="https://msdn.microsoft.com/c6df9842-9d69-4422-a8bc-c541ae31f21d">QuotaUsed</a>


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




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/80c01faf-717e-4375-8772-c61f04a7d7f3">IFsrmQuotaObject</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

