---
UID: NF:locationapi.ICivicAddressReport.GetAddressLine1
title: ICivicAddressReport::GetAddressLine1
author: windows-sdk-content
description: Retrieves the first line of a street address.
old-location: winlocation_com_ref\icivicaddressreport_getaddressline1.htm
old-project: LocationAPI
ms.assetid: 946f0e69-7139-45e9-8da4-755225ce1bd1
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetAddressLine1, GetAddressLine1 method [WinLocation], GetAddressLine1 method [WinLocation],ICivicAddressReport interface, ICivicAddressReport interface [WinLocation],GetAddressLine1 method, ICivicAddressReport.GetAddressLine1, ICivicAddressReport::GetAddressLine1, WinLocation_COM_Ref.icivicaddressreport_getaddressline1, locationapi/ICivicAddressReport::GetAddressLine1
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
 - ICivicAddressReport.GetAddressLine1
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ICivicAddressReport::GetAddressLine1


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Retrieves the first line of a street address.


## -parameters




### -param pbstrAddress1 [out]

Address of a <b>BSTR</b> that receives the first line of a street address.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ba8c66cb-be94-4649-ada9-620ed3b35516">ICivicAddressReport</a>
 

 

