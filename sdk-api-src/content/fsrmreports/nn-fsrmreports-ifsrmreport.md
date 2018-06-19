---
UID: NN:fsrmreports.IFsrmReport
title: IFsrmReport
author: windows-sdk-content
description: Used to configure the description and filters for a single report.
old-location: fsrm\ifsrmreport.htm
old-project: Fsrm
ms.assetid: 2172a543-b3b7-453e-887b-05c8ee74f197
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFsrmReport, IFsrmReport interface [File Server Resource Manager], IFsrmReport interface [File Server Resource Manager],described, fs.ifsrmreport, fsrm.ifsrmreport, fsrm/IFsrmReport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrmreports.h
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
 - IFsrmReport
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReport interface


## -description


Used to configure the description and filters for a single report.

To create this interface, call the <a href="https://msdn.microsoft.com/484941d1-726c-4765-8652-bcb378f277b4">IFsrmReportJob::CreateReport</a> method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/a1292084-f1b5-43eb-9b59-fa2f3f99557d">IFsrmReportJob::EnumReports</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReport</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmReport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmReport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b50139bc-c584-4bed-bf2e-34f1fef16e6d">Delete</a>
</td>
<td align="left" width="63%">
Removes this report object from the report job object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/991b0009-7ed9-4d75-af03-1b76aa8be70c">GetFilter</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the specified report filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d36e3e2-7826-4bae-943c-3ab73404534c">SetFilter</a>
</td>
<td align="left" width="63%">
Sets the current value of the specified report filter.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReport</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the description of the report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7aff8040-5d67-42a0-89ba-028cf39bd40a">LastGeneratedFileNamePrefix</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the report's generated file name for the last time the report was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the name of the report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the type of report to generate.

</td>
</tr>
</table> 

