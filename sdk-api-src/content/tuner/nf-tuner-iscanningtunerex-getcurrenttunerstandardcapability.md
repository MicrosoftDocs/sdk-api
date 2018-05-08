---
UID: NF:tuner.IScanningTunerEx.GetCurrentTunerStandardCapability
title: IScanningTunerEx::GetCurrentTunerStandardCapability
author: windows-driver-content
description: This topic applies to Windows Vista and later.
old-location: mstv\iscanningtunerex_getcurrenttunerstandardcapability.htm
old-project: mstv
ms.assetid: 4a3edf23-d782-4bfb-84c2-33eab7cb9d19
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetCurrentTunerStandardCapability, GetCurrentTunerStandardCapability method [Microsoft TV Technologies], GetCurrentTunerStandardCapability method [Microsoft TV Technologies],IScanningTunerEx interface, IScanningTunerEx interface [Microsoft TV Technologies],GetCurrentTunerStandardCapability method, IScanningTunerEx.GetCurrentTunerStandardCapability, IScanningTunerEx::GetCurrentTunerStandardCapability, IScanningTunerExGetCurrentTunerStandardCapability, mstv.iscanningtunerex_getcurrenttunerstandardcapability, tuner/IScanningTunerEx::GetCurrentTunerStandardCapability
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tuner.h
api_name:
-	IScanningTunerEx.GetCurrentTunerStandardCapability
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

