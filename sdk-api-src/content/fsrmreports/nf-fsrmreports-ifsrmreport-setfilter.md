---
UID: NF:fsrmreports.IFsrmReport.SetFilter
title: IFsrmReport::SetFilter (fsrmreports.h)
description: Sets the current value of the specified report filter.
helpviewer_keywords: ["IFsrmReport interface [File Server Resource Manager]","SetFilter method","IFsrmReport.SetFilter","IFsrmReport::SetFilter","SetFilter","SetFilter method [File Server Resource Manager]","SetFilter method [File Server Resource Manager]","IFsrmReport interface","fs.ifsrmreport_setfilter","fsrm.ifsrmreport_setfilter","fsrmreports/IFsrmReport::SetFilter"]
old-location: fsrm\ifsrmreport_setfilter.htm
tech.root: fsrm
ms.assetid: 6d36e3e2-7826-4bae-943c-3ab73404534c
ms.date: 12/05/2018
ms.keywords: IFsrmReport interface [File Server Resource Manager],SetFilter method, IFsrmReport.SetFilter, IFsrmReport::SetFilter, SetFilter, SetFilter method [File Server Resource Manager], SetFilter method [File Server Resource Manager],IFsrmReport interface, fs.ifsrmreport_setfilter, fsrm.ifsrmreport_setfilter, fsrmreports/IFsrmReport::SetFilter
req.header: fsrmreports.h
req.include-header: 
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
 - IFsrmReport::SetFilter
 - fsrmreports/IFsrmReport::SetFilter
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
 - IFsrmReport.SetFilter
---

# IFsrmReport::SetFilter


## -description

Sets the current value of the specified report filter.

## -parameters

### -param filter [in]

The filter used to  limit the files listed in a report. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportfilter">FsrmReportFilter</a> enumeration.

### -param filterValue [in]

The filter value to use for the specified report filter. The filter value cannot contain the following: 
      slash mark (/), backslash (\\), greater than sign (&gt;), less than sign (&lt;), vertical bar (|), double 
      quote ("), or colon (:).

## -returns

The method returns the following return values.

## -remarks

The filter value overrides the default value set using the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-setdefaultfilter">IFsrmReportManager::SetDefaultFilter</a> 
    method.

Note that each report type supports a specific set of filters. To determine if the filter is valid for the 
    report type, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmreports/nf-fsrmreports-ifsrmreportmanager-isfiltervalidforreporttype">IFsrmReportManager::IsFilterValidForReportType</a> 
    method.

The following list lists the variant types associated with the 
    <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmreportfilter">FsrmReportFilter</a> enumeration values used for the 
    <i>filter</i> parameter.

<table>
<tr>
<th>Filter type</th>
<th>Variant type</th>
</tr>
<tr>
<td><b>FsrmReportFilter_FileGroups</b></td>
<td>
<b>VT_BSTR</b> | <b>VT_ARRAY</b>. Set the 
       <b>parray</b> member of the variant.

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
<b>VT_BSTR</b> | <b>VT_ARRAY</b>. Set the 
       <b>parray</b> member of the variant.

</td>
</tr>
<tr>
<td><b>FsrmReportFilter_Property</b></td>
<td>
<b>VT_BSTR</b>. Set the <b>bstrVal</b> member of the variant.

</td>
</tr>
</table>
 


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/adding-a-report-to-a-job">Adding a Report to a Job</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmreport">IFsrmReport</a>