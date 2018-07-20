---
UID: NN:fsrmquota.IFsrmAutoApplyQuota
title: IFsrmAutoApplyQuota
author: windows-sdk-content
description: Used to automatically add the quota to new and existing subdirectories of the directory on which the automatic quota is applied.
old-location: fsrm\ifsrmautoapplyquota.htm
old-project: fsrm
ms.assetid: 3eb30caa-ce29-4898-b1a7-bd905031ca98
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IFsrmAutoApplyQuota, IFsrmAutoApplyQuota interface [File Server Resource Manager], IFsrmAutoApplyQuota interface [File Server Resource Manager],described, fs.ifsrmautoapplyquota, fsrm.ifsrmautoapplyquota, fsrm/IFsrmAutoApplyQuota
ms.prod: windows
ms.technology: windows-sdk
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
 - IFsrmAutoApplyQuota
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmAutoApplyQuota interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/3941d07c-67e3-4763-8113-31fc156c9bd0">MSFT_FSRMAutoQuota</a> class.]

Used to automatically add the quota to new and existing subdirectories of the directory on which the 
    automatic quota is applied.

To create an automatic quota, call the 
    <a href="https://msdn.microsoft.com/faaa55ca-a0b1-4cd4-9c73-20d80879b10c">IFsrmQuotaManager::CreateAutoApplyQuota</a> 
    method.

To retrieve this interface to an existing automatic quota, call one of the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/6542bc4e-535f-4e6c-aaa8-ba6963490811">IFsrmQuotaManager::EnumAutoApplyQuotas</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e6a4645c-c323-4c28-a284-9ebb677aeebb">IFsrmQuotaManager::GetAutoApplyQuota</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmAutoApplyQuota</b> interface inherits from <a href="https://msdn.microsoft.com/80c01faf-717e-4375-8772-c61f04a7d7f3">IFsrmQuotaObject</a>. <b>IFsrmAutoApplyQuota</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f988b78d-214a-4f4f-81d4-d7f59fecb02a">CommitAndUpdateDerived</a>
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

<a href="https://msdn.microsoft.com/1682e53c-f494-4fa4-b192-203b76e47394">ExcludeFolders</a>


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
    <a href="https://msdn.microsoft.com/fecb034f-3f11-4d37-9468-56d4ea6268e7">IFsrmQuotaTemplate::CommitAndUpdateDerived</a> 
    method to update the properties of the automatic quotas and the quotas that derive from the automatic quota.

If any quota under the automatic quota's path was changed to a different template, it will not be changed to 
    the automatic quota's new settings until you call the 
    <a href="https://msdn.microsoft.com/f988b78d-214a-4f4f-81d4-d7f59fecb02a">IFsrmAutoApplyQuota::CommitAndUpdateDerived</a> 
    method.

Changes made to the automatic quota are reflected in new quotas only after the automatic quota is 
    <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">committed</a>.




## -see-also




<a href="https://msdn.microsoft.com/09f0b952-e24f-4388-8e82-6b34145f9ad4">IFsrmQuotaManager::CreateQuota</a>



<a href="https://msdn.microsoft.com/80c01faf-717e-4375-8772-c61f04a7d7f3">IFsrmQuotaObject</a>



<a href="https://msdn.microsoft.com/3941d07c-67e3-4763-8113-31fc156c9bd0">MSFT_FSRMAutoQuota</a>
 

 

