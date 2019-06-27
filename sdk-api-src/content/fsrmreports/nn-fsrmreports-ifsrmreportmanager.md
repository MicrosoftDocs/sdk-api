---
UID: NN:fsrmreports.IFsrmReportManager
title: IFsrmReportManager (fsrmreports.h)
author: windows-sdk-content
description: Used to manage report jobs.
old-location: fsrm\ifsrmreportmanager.htm
tech.root: fsrm
ms.assetid: 112ed457-1083-4550-abd6-933f4b128e9a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmReportManager, IFsrmReportManager interface [File Server Resource Manager], IFsrmReportManager interface [File Server Resource Manager],described, fs.ifsrmreportmanager, fsrm.ifsrmreportmanager, fsrmreports/IFsrmReportManager
ms.topic: interface
f1_keywords: 
 - "fsrmreports/IFsrmReportManager"
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
 - IFsrmReportManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmReportManager interface


## -description


Used to manage report jobs.

To get this interface, call the 
    <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a> function. Use 
    <b>CLSID_FsrmReportManager</b> as the class identifier and 
    <code>__uuidof(IFsrmReportManager)</code> as the interface identifier. For 
    an example, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/defining-a-report-job">Defining a Report Job</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmReportManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IFsrmReportManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-createreportjob">CreateReportJob</a>
</td>
<td align="left" width="63%">
Creates a report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-enumreportjobs">EnumReportJobs</a>
</td>
<td align="left" width="63%">
Enumerates the report jobs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getdefaultfilter">GetDefaultFilter</a>
</td>
<td align="left" width="63%">
Retrieves the default report filter value that is used with the specified report type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getoutputdirectory">GetOutputDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the local directory path where the reports with the specified context are stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getreportjob">GetReportJob</a>
</td>
<td align="left" width="63%">
Retrieves the specified report job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-getreportsizelimit">GetReportSizeLimit</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the specified report size limit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-isfiltervalidforreporttype">IsFilterValidForReportType</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether a specified report filter is configurable for the specified report 
     type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setdefaultfilter">SetDefaultFilter</a>
</td>
<td align="left" width="63%">
Sets the default report filter value to use with the specified report type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setoutputdirectory">SetOutputDirectory</a>
</td>
<td align="left" width="63%">
Sets the local directory path where the reports with the specified context are stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setreportsizelimit">SetReportSizeLimit</a>
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>
 

 

