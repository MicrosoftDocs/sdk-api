---
UID: NN:fsrmreports.IFsrmReportManager
title: IFsrmReportManager
author: windows-sdk-content
description: Used to manage report jobs.
old-location: fsrm\ifsrmreportmanager.htm
old-project: Fsrm
ms.assetid: 112ed457-1083-4550-abd6-933f4b128e9a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFsrmReportManager, IFsrmReportManager interface [File Server Resource Manager], IFsrmReportManager interface [File Server Resource Manager],described, fs.ifsrmreportmanager, fsrm.ifsrmreportmanager, fsrmreports/IFsrmReportManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrmreports.h
req.include-header: FsrmReports.h, FsrmTlb.h
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
 - IFsrmReportManager
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmReportManager interface


## -description


Used to manage report jobs.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmReportManager</b> as the class identifier and 
    <code>__uuidof(IFsrmReportManager)</code> as the interface identifier. For 
    an example, see <a href="https://msdn.microsoft.com/a91c4fe7-ec8c-4d2b-b565-559e16668c87">Defining a Report Job</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReportManager</b> interface inherits from the <a href="http://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmReportManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmReportManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30274108-a820-409e-ba7c-6971b7726b9b">CreateReportJob</a>
</td>
<td align="left" width="63%">
Creates a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af66beb6-e82c-47e6-8658-da9702041053">EnumReportJobs</a>
</td>
<td align="left" width="63%">
Enumerates the report jobs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f3a587e-c3a8-47ee-80ac-afa0824a4585">GetDefaultFilter</a>
</td>
<td align="left" width="63%">
Retrieves the default report filter value that is used with the specified report type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90df1a6e-e2e6-4095-8337-61bfd172e203">GetOutputDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the local directory path where the reports with the specified context are stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60a1387f-a25f-4026-a582-71981c26dd1b">GetReportJob</a>
</td>
<td align="left" width="63%">
Retrieves the specified report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fe2546c-d70c-466a-8640-77cc2403a91d">GetReportSizeLimit</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the specified report size limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9f93b97-c8ac-441a-9f6b-87d45bd10cdf">IsFilterValidForReportType</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether a specified report filter is configurable for the specified report 
     type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a3165a9-8161-4dad-b8b9-d0c3f54f1803">SetDefaultFilter</a>
</td>
<td align="left" width="63%">
Sets the default report filter value to use with the specified report type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bbc4255-1fed-45c5-bb13-41ee7c47ed56">SetOutputDirectory</a>
</td>
<td align="left" width="63%">
Sets the local directory path where the reports with the specified context are stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d5a73ab-eccb-42e5-8796-d2986deccd34">SetReportSizeLimit</a>
</td>
<td align="left" width="63%">
Sets the current value of the specified report size limit.

</td>
</tr>
</table> 


## -remarks



A storage report job specifies a set of directories that will be analyzed to generate one or more different 
    report types that help administrators to better understand how storage is utilized in the specified directories. 
    You can configure report jobs to execute according to a schedule or on demand.

To create this object from a script, use the "Fsrm.FsrmReportManager" program 
    identifier.




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>
 

 

