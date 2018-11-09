---
UID: NF:locationapi.ILatLongReport.GetAltitudeError
title: ILatLongReport::GetAltitudeError
author: windows-sdk-content
description: Retrieves the altitude error, in meters.
old-location: winlocation_com_ref\ilatlongreport_getaltitudeerror.htm
tech.root: locationapi
ms.assetid: 313aefda-785c-43ce-a71c-cacfd929e27e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetAltitudeError, GetAltitudeError method [WinLocation], GetAltitudeError method [WinLocation],ILatLongReport interface, ILatLongReport interface [WinLocation],GetAltitudeError method, ILatLongReport.GetAltitudeError, ILatLongReport::GetAltitudeError, WinLocation_COM_Ref.ilatlongreport_getaltitudeerror, locationapi/ILatLongReport::GetAltitudeError
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ILatLongReport.GetAltitudeError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILatLongReport::GetAltitudeError


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Retrieves the altitude error, in meters.


## -parameters




### -param pAltitudeError [out]

Address of a <b>DOUBLE</b> that receives the altitude error, in meters. May be <b>NULL</b>.


## -returns



Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The method returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>HRESULT_FROM_WIN32(ERROR_NO_DATA)</dt>
</dl>
</td>
<td width="60%">
The location report does not include data for the requested field. This result is returned when the location sensor does not support altitude.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b489959e-74c7-46df-b63f-7d37e3a244d5">ILatLongReport</a>
 

 

