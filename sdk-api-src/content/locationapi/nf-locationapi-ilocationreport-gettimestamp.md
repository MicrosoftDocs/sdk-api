---
UID: NF:locationapi.ILocationReport.GetTimestamp
title: ILocationReport::GetTimestamp (locationapi.h)
description: Retrieves the date and time when the report was generated.
helpviewer_keywords: ["GetTimestamp","GetTimestamp method [WinLocation]","GetTimestamp method [WinLocation]","ILocationReport interface","ILocationReport interface [WinLocation]","GetTimestamp method","ILocationReport.GetTimestamp","ILocationReport::GetTimestamp","WinLocation_COM_Ref.ilocationreport_gettimestamp","locationapi/ILocationReport::GetTimestamp"]
old-location: winlocation_com_ref\ilocationreport_gettimestamp.htm
tech.root: winlocation
ms.assetid: 3573b2e7-fa76-4819-894d-d1215dc625bc
ms.date: 12/05/2018
ms.keywords: GetTimestamp, GetTimestamp method [WinLocation], GetTimestamp method [WinLocation],ILocationReport interface, ILocationReport interface [WinLocation],GetTimestamp method, ILocationReport.GetTimestamp, ILocationReport::GetTimestamp, WinLocation_COM_Ref.ilocationreport_gettimestamp, locationapi/ILocationReport::GetTimestamp
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILocationReport::GetTimestamp
 - locationapi/ILocationReport::GetTimestamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocationReport.GetTimestamp
---

# ILocationReport::GetTimestamp


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the date and time when the report was generated.

## -parameters

### -param pCreationTime [out]

Address of a <b>SYSTEMTIME</b> that receives the date and time when the report was generated. Time stamps are provided as Coordinated Universal Time (UTC).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a>