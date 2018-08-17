---
UID: NN:fsrmquota.IFsrmQuotaTemplateManager
title: IFsrmQuotaTemplateManager
author: windows-sdk-content
description: Used to manage quota templates.
old-location: fsrm\ifsrmquotatemplatemanager.htm
old-project: fsrm
ms.assetid: c6e782ff-b2e7-4bd6-bd9f-cc645c6ee5d6
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmQuotaTemplateManager, IFsrmQuotaTemplateManager interface [File Server Resource Manager], IFsrmQuotaTemplateManager interface [File Server Resource Manager],described, fs.ifsrmquotatemplatemanager, fsrm.ifsrmquotatemplatemanager, fsrmquota/IFsrmQuotaTemplateManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
req.redist: 
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
 - IFsrmQuotaTemplateManager
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaTemplateManager interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Used to manage quota templates.

To get this interface, call the 
    <a href="_com_CoCreateInstanceEx">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmQuotaTemplateManager</b> as the class identifier and 
    <code>__uuidof(IFsrmQuotaTemplateManager)</code> as the interface 
    identifier. For an example, see 
    <a href="https://msdn.microsoft.com/88ff3968-cb83-4b66-83e9-a58205b4be82">Using Templates to Define Quotas</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaTemplateManager</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmQuotaTemplateManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmQuotaTemplateManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8dbc0fb-de02-4491-94f5-e845a2338251">CreateTemplate</a>
</td>
<td align="left" width="63%">
Creates a quota template object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5f5b94a-6b17-4379-9141-07ec70a830e9">EnumTemplates</a>
</td>
<td align="left" width="63%">
Enumerates the quota templates on the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36ba071b-4db2-42fb-90a8-838c45dfdd16">ExportTemplates</a>
</td>
<td align="left" width="63%">
Exports the quota templates as an XML string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2877c453-aad7-42ea-a66d-b49ab1f8f854">GetTemplate</a>
</td>
<td align="left" width="63%">
Retrieves the specified quota template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f530d7fc-8b41-4a5e-a10a-b9211c7fe2bb">ImportTemplates</a>
</td>
<td align="left" width="63%">
Imports the specified quota templates from an XML string.

</td>
</tr>
</table> 


## -remarks



Note that a new installation of the operating system includes FSRM-defined templates.

To create this object from a script, use the "Fsrm.FsrmQuotaTemplateManager" program 
    identifier.




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/954dbbae-78b1-4530-af2d-a1fe0d23b83f">FsrmQuotaTemplateManager</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

