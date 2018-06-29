---
UID: NF:locationapi.ILatLongReport.GetErrorRadius
title: ILatLongReport::GetErrorRadius
author: windows-sdk-content
description: Retrieves a distance from the reported location, in meters. Combined with the location reported as the origin, this radius describes the circle in which the actual location is probably located.
old-location: winlocation_com_ref\ilatlongreport_geterrorradius.htm
old-project: LocationAPI
ms.assetid: cb0941da-607d-4082-ac8c-91d2edafa8ab
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetErrorRadius, GetErrorRadius method [WinLocation], GetErrorRadius method [WinLocation],ILatLongReport interface, ILatLongReport interface [WinLocation],GetErrorRadius method, ILatLongReport.GetErrorRadius, ILatLongReport::GetErrorRadius, WinLocation_COM_Ref.ilatlongreport_geterrorradius, locationapi/ILatLongReport::GetErrorRadius
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
 - ILatLongReport.GetErrorRadius
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILatLongReport::GetErrorRadius


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Retrieves a distance from the reported location, in meters. Combined with the location reported as the origin, this radius describes the circle in which the actual location is probably located.


## -parameters




### -param pErrorRadius [out]

Address of a <b>DOUBLE</b> that receives the error radius.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b489959e-74c7-46df-b63f-7d37e3a244d5">ILatLongReport</a>
 

 

