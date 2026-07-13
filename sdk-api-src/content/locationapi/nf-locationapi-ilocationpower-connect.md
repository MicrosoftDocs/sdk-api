---
UID: NF:locationapi.ILocationPower.Connect
title: ILocationPower::Connect (locationapi.h)
description: Used by Windows Store app browsers in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect). (ILocationPower.Connect)
helpviewer_keywords: ["Connect","Connect method [WinLocation]","Connect method [WinLocation]","ILocationPower interface","ILocationPower interface [WinLocation]","Connect method","ILocationPower.Connect","ILocationPower::Connect","WinLocation_COM_Ref.ilocationpower_connect","locationapi/ILocationPower::Connect","winlocation.ilocationpower_connect"]
old-location: winlocation_com_ref\ilocationpower_connect.htm
tech.root: winlocation
ms.assetid: 6c0145e0-974e-42b2-936e-9396f5c96e72
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [WinLocation], Connect method [WinLocation],ILocationPower interface, ILocationPower interface [WinLocation],Connect method, ILocationPower.Connect, ILocationPower::Connect, WinLocation_COM_Ref.ilocationpower_connect, locationapi/ILocationPower::Connect, winlocation.ilocationpower_connect
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: LocationApi.idl
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
 - ILocationPower::Connect
 - locationapi/ILocationPower::Connect
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
 - ILocationPower.Connect
---

# ILocationPower::Connect


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Used by Windows Store app browsers  in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect).

Most apps will not need to use this method.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationpower">ILocationPower</a>
