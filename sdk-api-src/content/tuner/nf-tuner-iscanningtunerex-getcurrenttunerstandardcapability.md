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

# IScanningTunerEx::GetCurrentTunerStandardCapability


## -description



This topic applies to Windows Vista and later.
        



The <b>GetCurrentTunerStandardCapability</b> method retrieves the tuner's capabilities for a specified broadcast standard.


## -parameters




### -param CurrentBroadcastStandard [in]

GUID that specifies the broadcast standard to query. To find the broadcast standards supported by the tuner, call <a href="https://msdn.microsoft.com/7dc7aeec-2a9d-4dfb-9f67-36d8131cc130">GetTunerScanningCapability</a>.


### -param SettlingTime [out]

Receives the approximate amount of time the tuner requires to tune to a frequency, in milliseconds.


### -param TvStandardsSupported [out]

If <i>CurrentBroadcastStandard</i> is ANALOG_TV_NETWORK_TYPE, this parameter receives a bitwise OR of flags from the <a href="https://msdn.microsoft.com/6760a40c-550c-4774-a5d1-d7e2a6aa6096">AnalogVideoStandard</a> enumeration, indicating which analog television formats are supported by the tuner. Otherwise, this parameter is ignored.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3f89173a-d24b-400c-a229-28efb7a703be">IScanningTunerEx Interface</a>
 

 

