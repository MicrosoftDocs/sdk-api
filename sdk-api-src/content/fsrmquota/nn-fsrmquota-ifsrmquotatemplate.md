---
UID: NN:fsrmquota.IFsrmQuotaTemplate
title: IFsrmQuotaTemplate
author: windows-sdk-content
description: Used to configure templates from which new quota objects can be derived.
old-location: fsrm\ifsrmquotatemplate.htm
old-project: Fsrm
ms.assetid: de8ac383-f309-4320-bc77-c859ba27e1ca
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: IFsrmQuotaTemplate, IFsrmQuotaTemplate interface [File Server Resource Manager], IFsrmQuotaTemplate interface [File Server Resource Manager],described, fs.ifsrmquotatemplate, fsrm.ifsrmquotatemplate, fsrm/IFsrmQuotaTemplate
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmQuotaTemplate
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaTemplate interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Used to configure templates from which new quota objects can be derived. Templates are 
    identified by a name and are used to simplify the configuration of directory quotas.

To create this interface, call the 
    <a href="https://msdn.microsoft.com/d8dbc0fb-de02-4491-94f5-e845a2338251">IFsrmQuotaTemplateManager::CreateTemplate</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/e5f5b94a-6b17-4379-9141-07ec70a830e9">IFsrmQuotaTemplateManager::EnumTemplates</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2877c453-aad7-42ea-a66d-b49ab1f8f854">IFsrmQuotaTemplateManager::GetTemplate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f530d7fc-8b41-4a5e-a10a-b9211c7fe2bb">IFsrmQuotaTemplateManager::ImportTemplates</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaTemplate</b> interface inherits from <a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>. <b>IFsrmQuotaTemplate</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fecb034f-3f11-4d37-9468-56d4ea6268e7">CommitAndUpdateDerived</a>
</td>
<td align="left" width="63%">
Saves the quota template and then applies any changes to the derived quota objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00aa7693-3c6e-4688-915e-59c31e5b8e6e">CopyTemplate</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


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




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

