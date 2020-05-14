---
UID: NF:tuner.IScanningTunerEx.GetCurrentTunerStandardCapability
title: IScanningTunerEx::GetCurrentTunerStandardCapability (tuner.h)
description: This topic applies to Windows Vista and later.helpviewer_keywords: ["GetCurrentTunerStandardCapability","GetCurrentTunerStandardCapability method [Microsoft TV Technologies]","GetCurrentTunerStandardCapability method [Microsoft TV Technologies]","IScanningTunerEx interface","IScanningTunerEx interface [Microsoft TV Technologies]","GetCurrentTunerStandardCapability method","IScanningTunerEx.GetCurrentTunerStandardCapability","IScanningTunerEx::GetCurrentTunerStandardCapability","IScanningTunerExGetCurrentTunerStandardCapability","mstv.iscanningtunerex_getcurrenttunerstandardcapability","tuner/IScanningTunerEx::GetCurrentTunerStandardCapability"]
old-location: mstv\iscanningtunerex_getcurrenttunerstandardcapability.htm
tech.root: mstv
ms.assetid: 4a3edf23-d782-4bfb-84c2-33eab7cb9d19
ms.date: 12/05/2018
ms.keywords: GetCurrentTunerStandardCapability, GetCurrentTunerStandardCapability method [Microsoft TV Technologies], GetCurrentTunerStandardCapability method [Microsoft TV Technologies],IScanningTunerEx interface, IScanningTunerEx interface [Microsoft TV Technologies],GetCurrentTunerStandardCapability method, IScanningTunerEx.GetCurrentTunerStandardCapability, IScanningTunerEx::GetCurrentTunerStandardCapability, IScanningTunerExGetCurrentTunerStandardCapability, mstv.iscanningtunerex_getcurrenttunerstandardcapability, tuner/IScanningTunerEx::GetCurrentTunerStandardCapability
f1_keywords:
- tuner/IScanningTunerEx.GetCurrentTunerStandardCapability
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tuner.h
api_name:
- IScanningTunerEx.GetCurrentTunerStandardCapability
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IScanningTunerEx::GetCurrentTunerStandardCapability


## -description



This topic applies to Windows Vista and later.
        



The <b>GetCurrentTunerStandardCapability</b> method retrieves the tuner's capabilities for a specified broadcast standard.


## -parameters




### -param CurrentBroadcastStandard [in]

GUID that specifies the broadcast standard to query. To find the broadcast standards supported by the tuner, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iscanningtunerex-gettunerscanningcapability">GetTunerScanningCapability</a>.


### -param SettlingTime [out]

Receives the approximate amount of time the tuner requires to tune to a frequency, in milliseconds.


### -param TvStandardsSupported [out]

If <i>CurrentBroadcastStandard</i> is ANALOG_TV_NETWORK_TYPE, this parameter receives a bitwise OR of flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-analogvideostandard">AnalogVideoStandard</a> enumeration, indicating which analog television formats are supported by the tuner. Otherwise, this parameter is ignored.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtunerex">IScanningTunerEx Interface</a>
 

 

