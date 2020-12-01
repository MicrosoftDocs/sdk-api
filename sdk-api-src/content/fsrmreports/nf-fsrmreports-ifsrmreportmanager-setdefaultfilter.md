---
UID: NF:fsrmreports.IFsrmReportManager.SetDefaultFilter
title: IFsrmReportManager::SetDefaultFilter (fsrmreports.h)
description: Sets the default report filter value to use with the specified report type.
helpviewer_keywords: ["FsrmReportManager class [File Server Resource Manager]","SetDefaultFilter method","IFsrmReportManager interface [File Server Resource Manager]","SetDefaultFilter method","IFsrmReportManager.SetDefaultFilter","IFsrmReportManager::SetDefaultFilter","SetDefaultFilter","SetDefaultFilter method [File Server Resource Manager]","SetDefaultFilter method [File Server Resource Manager]","FsrmReportManager class","SetDefaultFilter method [File Server Resource Manager]","IFsrmReportManager interface","fs.ifsrmreportmanager_setdefaultfilter","fsrm.ifsrmreportmanager_setdefaultfilter","fsrmreports/IFsrmReportManager::SetDefaultFilter"]
old-location: fsrm\ifsrmreportmanager_setdefaultfilter.htm
tech.root: fsrm
ms.assetid: 5a3165a9-8161-4dad-b8b9-d0c3f54f1803
ms.date: 12/05/2018
ms.keywords: FsrmReportManager class [File Server Resource Manager],SetDefaultFilter method, IFsrmReportManager interface [File Server Resource Manager],SetDefaultFilter method, IFsrmReportManager.SetDefaultFilter, IFsrmReportManager::SetDefaultFilter, SetDefaultFilter, SetDefaultFilter method [File Server Resource Manager], SetDefaultFilter method [File Server Resource Manager],FsrmReportManager class, SetDefaultFilter method [File Server Resource Manager],IFsrmReportManager interface, fs.ifsrmreportmanager_setdefaultfilter, fsrm.ifsrmreportmanager_setdefaultfilter, fsrmreports/IFsrmReportManager::SetDefaultFilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmReportManager::SetDefaultFilter
 - fsrmreports/IFsrmReportManager::SetDefaultFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmReportManager.SetDefaultFilter
 - FsrmReportManager.SetDefaultFilter
---

# IFsrmReportManager::SetDefaultFilter


## -description

Sets the default report filter value to use with the specified report type.

## -parameters

### -param reportType [in]

The report type. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreporttype">FsrmReportType</a> enumeration.

### -param filter [in]

The report filter. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportfilter">FsrmReportFilter</a> enumeration.

### -param filterValue [in]

The default report filter value.

## -returns

The method returns the following return values.

## -remarks

This value is used if the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreport-setfilter">IFsrmReport::SetFilter</a> method was not called to specify a filter value for the report.

Note that each report type supports a specific set of filters. To determine if the filter is valid, call the <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-isfiltervalidforreporttype">IFsrmReportManager::IsFilterValidForReportType</a> method.

The following list lists the variant types associated with the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportfilter">FsrmReportFilter</a> enumeration values used for the <i>filterValue</i> parameter.

<table>
<tr>
<th>Filter type</th>
<th>Variant type</th>
</tr>
<tr>
<td><b>FsrmReportFilter_FileGroups</b></td>
<td>
<b>VT_BSTR</b> | <b>VT_ARRAY</b>. Set the <b>parray</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_MinAgeDays</b></td>
<td>
<b>VT_I4</b>. Set the <b>lVal</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_MaxAgeDays</b></td>
<td>
<b>VT_I4</b>. Set the <b>lVal</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_MinQuotaUsage</b></td>
<td>
<b>VT_I4</b>. Set the <b>lVal</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_MinSize</b></td>
<td>
<b>VT_I8</b>. Set the <b>llVal</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_NamePattern</b></td>
<td>
<b>VT_BSTR</b>. Set the <b>bstrVal</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_Owners</b></td>
<td>
<b>VT_BSTR</b> | <b>VT_ARRAY</b>. Set the <b>parray</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_Property</b></td>
<td>
<b>VT_BSTR</b>. Set the <b>bstrVal</b> member of the variant.

</td>
</tr>
</table>
 

The default filter values are used for report actions.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmreportmanager">FsrmReportManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreportmanager">IFsrmReportManager</a>