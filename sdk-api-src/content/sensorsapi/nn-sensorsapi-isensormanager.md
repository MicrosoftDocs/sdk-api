---
UID: NN:sensorsapi.ISensorManager
title: ISensorManager
author: windows-driver-content
description: Provides methods for discovering and retrieving available sensors and a method to request sensor manager events.
old-location: winsensors\isensormanager.htm
old-project: SensorsAPI
ms.assetid: 313742c9-58a7-4ddd-9582-a6ee276e97d0
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ISensorManager, ISensorManager interface [WinSensors], ISensorManager interface [WinSensors], described, sensorsapi/ISensorManager, winsensors.isensormanager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: MagnetometerAccuracy
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sensorsapi.dll
api_name:
-	ISensorManager
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISensorManager interface


## -description


Provides methods for discovering and retrieving available sensors and a method to request sensor manager events.


## -remarks



You retrieve a pointer to this interface by calling the COM <b>CoCreateInstance</b> method. If group policy does not allow creation of this object, <b>CoCreateInstance</b> will return <b>HRESULT_FROM_WIN32
(ERROR_ACCESS_DISABLED_BY_POLICY)</b>.


#### Examples

The following example code creates an instance of the sensor manager. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Create the sensor manager.
hr = CoCreateInstance(CLSID_SensorManager, 
                        NULL, CLSCTX_INPROC_SERVER,
                        IID_PPV_ARGS(&amp;pSensorManager));

if(hr == HRESULT_FROM_WIN32(ERROR_ACCESS_DISABLED_BY_POLICY))
{
    // Unable to retrieve sensor manager due to 
    // group policy settings. Alert the user.
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt725374">COM Interfaces</a>
 

 

