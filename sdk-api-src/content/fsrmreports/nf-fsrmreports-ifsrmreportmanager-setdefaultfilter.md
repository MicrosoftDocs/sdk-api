---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFsrmReportManager::SetDefaultFilter


## -description


Sets the default report filter value to use with the specified report type.


## -parameters




### -param reportType [in]

The report type. For possible values, see the <a href="https://msdn.microsoft.com/6fb5cb02-371b-4d07-9f13-d0409d5835d4">FsrmReportType</a> enumeration.


### -param filter [in]

The report filter. For possible values, see the <a href="https://msdn.microsoft.com/6f38ec9a-8876-44ce-9d44-f3982f1880ca">FsrmReportFilter</a> enumeration.


### -param filterValue [in]

The default report filter value.


## -returns



The method returns the following return values.




## -remarks



This value is used if the <a href="https://msdn.microsoft.com/6d36e3e2-7826-4bae-943c-3ab73404534c">IFsrmReport::SetFilter</a> method was not called to specify a filter value for the report.

Note that each report type supports a specific set of filters. To determine if the filter is valid, call the <a href="https://msdn.microsoft.com/e9f93b97-c8ac-441a-9f6b-87d45bd10cdf">IFsrmReportManager::IsFilterValidForReportType</a> method.

The following list lists the variant types associated with the <a href="https://msdn.microsoft.com/6f38ec9a-8876-44ce-9d44-f3982f1880ca">FsrmReportFilter</a> enumeration values used for the <i>filterValue</i> parameter.

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




<a href="https://msdn.microsoft.com/308c5001-b84d-49ab-ae2c-f16466f9abca">FsrmReportManager</a>



<a href="https://msdn.microsoft.com/112ed457-1083-4550-abd6-933f4b128e9a">IFsrmReportManager</a>
 

 

