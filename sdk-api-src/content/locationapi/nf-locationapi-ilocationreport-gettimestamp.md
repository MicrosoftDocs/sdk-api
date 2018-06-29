---
UID: NF:locationapi.ILocationReport.GetTimestamp
title: ILocationReport::GetTimestamp
author: windows-sdk-content
description: Retrieves the date and time when the report was generated.
old-location: winlocation_com_ref\ilocationreport_gettimestamp.htm
old-project: LocationAPI
ms.assetid: 3573b2e7-fa76-4819-894d-d1215dc625bc
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetTimestamp, GetTimestamp method [WinLocation], GetTimestamp method [WinLocation],ILocationReport interface, ILocationReport interface [WinLocation],GetTimestamp method, ILocationReport.GetTimestamp, ILocationReport::GetTimestamp, WinLocation_COM_Ref.ilocationreport_gettimestamp, locationapi/ILocationReport::GetTimestamp
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
 - ILocationReport.GetTimestamp
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocationReport::GetTimestamp


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Retrieves the date and time when the report was generated.


## -parameters




### -param pCreationTime [out]

Address of a <b>SYSTEMTIME</b> that receives the date and time when the report was generated. Time stamps are provided as Coordinated Universal Time (UTC).


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6dc78c26-36b3-4545-b5ba-7f04f6e67706">ILocationReport</a>
 

 

