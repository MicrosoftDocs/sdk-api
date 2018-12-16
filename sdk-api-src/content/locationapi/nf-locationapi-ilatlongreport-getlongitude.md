---
UID: NF:locationapi.ILatLongReport.GetLongitude
title: ILatLongReport::GetLongitude
author: windows-sdk-content
description: Retrieves the longitude, in degrees.
old-location: winlocation_com_ref\ilatlongreport_getlongitude.htm
tech.root: locationapi
ms.assetid: 77fa407b-109c-45aa-bbdb-0b8a40d222e5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLongitude, GetLongitude method [WinLocation], GetLongitude method [WinLocation],ILatLongReport interface, ILatLongReport interface [WinLocation],GetLongitude method, ILatLongReport.GetLongitude, ILatLongReport::GetLongitude, WinLocation_COM_Ref.ilatlongreport_getlongitude, locationapi/ILatLongReport::GetLongitude
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
 - ILatLongReport.GetLongitude
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILatLongReport::GetLongitude


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Retrieves the longitude, in degrees. The longitude is between -180 and 180, where East is positive.
      


## -parameters




### -param pLongitude [out]

Address of a <b>DOUBLE</b> that receives the longitude.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b489959e-74c7-46df-b63f-7d37e3a244d5">ILatLongReport</a>
 

 

