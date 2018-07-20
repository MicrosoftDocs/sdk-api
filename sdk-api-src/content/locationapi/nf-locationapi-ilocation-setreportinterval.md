---
UID: NF:locationapi.ILocation.SetReportInterval
title: ILocation::SetReportInterval
author: windows-sdk-content
description: Specifies the requested minimum amount of time, in milliseconds, between report events.
old-location: winlocation_com_ref\ilocation_setreportinterval.htm
old-project: locationapi
ms.assetid: 4b48f64d-47e8-41cc-a7a1-970654896e7e
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: ILocation interface [WinLocation],SetReportInterval method, ILocation.SetReportInterval, ILocation::SetReportInterval, SetReportInterval, SetReportInterval method [WinLocation], SetReportInterval method [WinLocation],ILocation interface, WinLocation_COM_Ref.ilocation_setreportinterval, locationapi/ILocation::SetReportInterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only],Windows 7
req.target-min-winversvr: None supported
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
req.typenames: LOCATION_REPORT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocation.SetReportInterval
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocation::SetReportInterval


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Specifies the requested minimum amount of time, in milliseconds, between report events.


## -parameters




### -param reportType [in]

<b>REFIID</b> that specifies the report type for which to set the interval.


### -param millisecondsRequested [in]

<b>DWORD</b> that contains the report interval value, in milliseconds. If this value is zero, no minimum interval is specified and your application receives events at the location sensor's default interval.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The caller is not registered to receive events for the specified report type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
<i>reportType</i> was other than <b>IID_ILatLongReport</b> or <b>IID_ICivicAddressReport</b>.

</td>
</tr>
</table>
 




## -remarks



The interval you request by using this method represents the shortest amount of time between events. This means that you request to receive event notifications no more frequently than specified, but the elapsed time may be significantly longer. Use this method to help ensure that event notifications do not use more processor resources than necessary.

It is not guaranteed that your request for a particular report interval will be set by the location provider. Call <a href="https://msdn.microsoft.com/c7bcd665-317c-428a-aa20-0d09c8d7a813">GetReportInterval </a>to discover the true report interval setting.

A report interval of zero means that no minimum interval is specified, and the application may receive events at the frequency that the location sensor sends events.


#### Examples

The following example demonstrates how to call <b>SetReportInterval</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Set the latitude/longitude report interval to 1000 milliseconds
HRESULT hr = spLocation-&gt;SetReportInterval(IID_ILatLongReport, 1000);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/beeedbbd-df93-4c05-a215-4cfd14e03076">ILocation</a>
 

 

