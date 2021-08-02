---
UID: NF:locationapi.ILocationReport.GetSensorID
title: ILocationReport::GetSensorID (locationapi.h)
description: Retrieves the ID of the sensor that generated the location report.
helpviewer_keywords: ["GetSensorID","GetSensorID method [WinLocation]","GetSensorID method [WinLocation]","ILocationReport interface","ILocationReport interface [WinLocation]","GetSensorID method","ILocationReport.GetSensorID","ILocationReport::GetSensorID","WinLocation_COM_Ref.ilocationreport_getsensorid","locationapi/ILocationReport::GetSensorID"]
old-location: winlocation_com_ref\ilocationreport_getsensorid.htm
tech.root: winlocation
ms.assetid: c75b2ce3-8c60-4e26-870f-2bec599ea3b8
ms.date: 12/05/2018
ms.keywords: GetSensorID, GetSensorID method [WinLocation], GetSensorID method [WinLocation],ILocationReport interface, ILocationReport interface [WinLocation],GetSensorID method, ILocationReport.GetSensorID, ILocationReport::GetSensorID, WinLocation_COM_Ref.ilocationreport_getsensorid, locationapi/ILocationReport::GetSensorID
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
 - ILocationReport::GetSensorID
 - locationapi/ILocationReport::GetSensorID
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
 - ILocationReport.GetSensorID
---

# ILocationReport::GetSensorID


## -description

<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a> API.
]

Retrieves the ID of the sensor that generated the location report.

## -parameters

### -param pSensorID [out]

Address of a <b>SENSOR_ID</b> that receives the ID of the sensor that generated the location report.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A sensor ID is a <b>GUID</b>.


#### Examples

The following example demonstrates how to call <b>GetSensorID</b>.


```cpp
    // Print the Sensor ID GUID
    GUID sensorID = {0};
    if (SUCCEEDED(spLatLongReport->GetSensorID(&sensorID)))
    {
        wprintf(L"SensorID: %s\n", GUIDToString(sensorID, szGUID, ARRAYSIZE(szGUID)));
    }

```

## -see-also

<a href="/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a>