---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetMonitorRedGreenOrBlueGain function


## -description



        Sets a monitor's red, green, or blue gain value.


## -parameters




### -param hMonitor [in]


            Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param gtGainType [in]


            A member of the <a href="https://msdn.microsoft.com/330b7891-bc65-4c78-bb43-f8fcd2a6b1c3">MC_GAIN_TYPE</a> enumeration, specifying whether to set the red, green, or blue gain.
          


### -param dwNewGain [in]


            Red, green, or blue gain value. To get the monitor's minimum and maximum gain values, call <a href="https://msdn.microsoft.com/058d70c4-a29c-4916-a4b9-911db5863363">GetMonitorRedGreenOrBlueGain</a>.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call GetLastError.




## -remarks




        Gain settings are generally used to adjust the monitor's white point.
      


        If this function is supported, the <a href="https://msdn.microsoft.com/57cf0004-58cf-46d9-b5be-22edda2ce5a9">GetMonitorCapabilities</a> function returns the MC_CAPS_RED_GREEN_BLUE_GAIN flag.
      


        This function takes about 50 milliseconds to return.
      


        Changing the gain settings can change the color temperature. To get the new color temperature, call <a href="https://msdn.microsoft.com/872aabcc-b274-454c-a08b-6c4c5aa83012">GetMonitorColorTemperature</a>.
      


        The gain settings are continuous monitor settings. For more information, see <a href="https://msdn.microsoft.com/23e5d45d-a924-4119-b21d-b24764b53a94">Using the High-Level Monitor Configuration Functions</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

