---
UID: NF:locationapi.ILocation.GetDesiredAccuracy
title: ILocation::GetDesiredAccuracy
author: windows-sdk-content
description: Retrieves the current requested accuracy setting.
old-location: winlocation\ilocation_getdesiredaccuracy.htm
old-project: LocationAPI
ms.assetid: caa34e34-7370-4e42-9c0f-00498f5fc37d
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetDesiredAccuracy, GetDesiredAccuracy method [WinLocation], GetDesiredAccuracy method [WinLocation],ILocation interface, ILocation interface [WinLocation],GetDesiredAccuracy method, ILocation.GetDesiredAccuracy, ILocation::GetDesiredAccuracy, locationapi/ILocation::GetDesiredAccuracy, winlocation.ilocation_getdesiredaccuracy
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
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocation.GetDesiredAccuracy
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocation::GetDesiredAccuracy


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Retrieves the current requested accuracy setting.


## -parameters




### -param reportType [in]

<b>REFIID</b> that specifies the report type for which to get the requested accuracy.


### -param pDesiredAccuracy [out]

The address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545668">LOCATION_DESIRED_ACCURACY</a> that receives the accuracy value. If the report is not registered, this will be set to <b>NULL</b>.


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
<i>pDesiredAccuracy</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/beeedbbd-df93-4c05-a215-4cfd14e03076">ILocation</a>
 

 

