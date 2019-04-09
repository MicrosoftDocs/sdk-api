---
UID: NF:locationapi.ILocation.UnregisterForReport
title: ILocation::UnregisterForReport (locationapi.h)
author: windows-sdk-content
description: Stops event notifications for the specified report type.
old-location: winlocation_com_ref\ilocation_unregisterforreport.htm
tech.root: locationapi
ms.assetid: 333bd127-2c6a-4f09-9f86-4f8e68a9ea55
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILocation interface [WinLocation],UnregisterForReport method, ILocation.UnregisterForReport, ILocation::UnregisterForReport, UnregisterForReport, UnregisterForReport method [WinLocation], UnregisterForReport method [WinLocation],ILocation interface, WinLocation_COM_Ref.ilocation_unregisterforreport, locationapi/ILocation::UnregisterForReport
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
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocation.UnregisterForReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocation::UnregisterForReport


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Stops event notifications for the specified report type.


## -parameters




### -param reportType [in]

<b>REFIID</b> that specifies the interface ID of the report type for which to stop events. 


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
<i>reportType </i> is other than IID_ILatLongReport or IID_ICivicAddressReport. 

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/beeedbbd-df93-4c05-a215-4cfd14e03076">ILocation</a>
 

 

