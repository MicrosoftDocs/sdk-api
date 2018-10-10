---
UID: NF:locationapi.ILocationReport.GetSensorID
title: ILocationReport::GetSensorID
author: windows-sdk-content
description: Retrieves the ID of the sensor that generated the location report.
old-location: winlocation_com_ref\ilocationreport_getsensorid.htm
tech.root: LocationAPI
ms.assetid: c75b2ce3-8c60-4e26-870f-2bec599ea3b8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSensorID, GetSensorID method [WinLocation], GetSensorID method [WinLocation],ILocationReport interface, ILocationReport interface [WinLocation],GetSensorID method, ILocationReport.GetSensorID, ILocationReport::GetSensorID, WinLocation_COM_Ref.ilocationreport_getsensorid, locationapi/ILocationReport::GetSensorID
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
 - ILocationReport.GetSensorID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILocationReport::GetSensorID


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

Retrieves the ID of the sensor that generated the location report.


## -parameters




### -param pSensorID [out]

Address of a <b>SENSOR_ID</b> that receives the ID of the sensor that generated the location report.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A sensor ID is a <b>GUID</b>.


#### Examples

The following example demonstrates how to call <b>GetSensorID</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    // Print the Sensor ID GUID
    GUID sensorID = {0};
    if (SUCCEEDED(spLatLongReport-&gt;GetSensorID(&amp;sensorID)))
    {
        wprintf(L"SensorID: %s\n", GUIDToString(sensorID, szGUID, ARRAYSIZE(szGUID)));
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6dc78c26-36b3-4545-b5ba-7f04f6e67706">ILocationReport</a>
 

 

