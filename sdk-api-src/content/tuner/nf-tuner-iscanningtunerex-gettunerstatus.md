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

# IScanningTunerEx::GetTunerStatus


## -description



This topic applies to Windows Vista and later.
        



The <b>GetTunerStatus</b> method returns the current status of the most recent call to <a href="https://msdn.microsoft.com/35ed1b43-020e-4baa-9f15-eb316d9a137b">PerformExhaustiveScan</a>.


## -parameters




### -param SecondsLeft [out]

Receives the estimated number of seconds remaining for the scan to complete.


### -param CurrentLockType [out]

Receives a member of the <a href="https://msdn.microsoft.com/657dfd46-b01c-41aa-af0c-0d07235f15fc">TunerLockType</a> enumeration, indicating how well the tuner locked onto a signal.


### -param AutoDetect [out]

Receives a Boolean value. If the value is <b>TRUE</b>, the tuner is in auto-detect mode.


### -param CurrentFreq [out]

Receives the frequency that was most recently scanned.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



While the scan is in progress, the application can use this method to estimate the total time required for the scan to complete. When the tuner locks onto a frequency and sets the application's event handle, the application can use this method to find the locked frequency.




## -see-also




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

