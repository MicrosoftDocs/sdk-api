---
UID: NF:locationapi.ILocation.SetDesiredAccuracy
title: ILocation::SetDesiredAccuracy
author: windows-sdk-content
description: Specifies the accuracy to be used.
old-location: winlocation\ilocation_setdesiredaccuracy.htm
old-project: locationapi
ms.assetid: 85623570-3b48-42ea-babd-fe4282629d92
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ILocation interface [WinLocation],SetDesiredAccuracy method, ILocation.SetDesiredAccuracy, ILocation::SetDesiredAccuracy, SetDesiredAccuracy, SetDesiredAccuracy method [WinLocation], SetDesiredAccuracy method [WinLocation],ILocation interface, locationapi/ILocation::SetDesiredAccuracy, winlocation.ilocation_setdesiredaccuracy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - ILocation.SetDesiredAccuracy
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocation::SetDesiredAccuracy


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Specifies the accuracy to be used.


## -parameters




### -param reportType [in]

<b>REFIID</b> that specifies the report type for which to set the accuracy to be used.


### -param desiredAccuracy [in]


<a href="https://msdn.microsoft.com/library/windows/hardware/ff545668">LOCATION_DESIRED_ACCURACY</a> value that specifies the accuracy to be used.


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
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
<i>reportType</i> was other than <b>IID_ILatLongReport</b> or <b>IID_ICivicAddressReport</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>desiredAccuracy</i> is not supported in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff545668">LOCATION_DESIRED_ACCURACY</a> enumerated type.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/beeedbbd-df93-4c05-a215-4cfd14e03076">ILocation</a>
 

 

