---
UID: NF:bdaiface.IBDA_SignalStatistics.get_SampleTime
title: IBDA_SignalStatistics::get_SampleTime (bdaiface.h)
description: The get_SampleTime method retrieves the sample time used to measure the signal.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","get_SampleTime method","IBDA_SignalStatistics.get_SampleTime","IBDA_SignalStatistics::get_SampleTime","IBDA_SignalStatisticsget_SampleTime","bdaiface/IBDA_SignalStatistics::get_SampleTime","get_SampleTime","get_SampleTime method [Microsoft TV Technologies]","get_SampleTime method [Microsoft TV Technologies]","IBDA_SignalStatistics interface","mstv.ibda_signalstatistics_get_sampletime"]
old-location: mstv\ibda_signalstatistics_get_sampletime.htm
tech.root: mstv
ms.assetid: 9651e393-224b-4276-b8a6-f841f9e04d48
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],get_SampleTime method, IBDA_SignalStatistics.get_SampleTime, IBDA_SignalStatistics::get_SampleTime, IBDA_SignalStatisticsget_SampleTime, bdaiface/IBDA_SignalStatistics::get_SampleTime, get_SampleTime, get_SampleTime method [Microsoft TV Technologies], get_SampleTime method [Microsoft TV Technologies],IBDA_SignalStatistics interface, mstv.ibda_signalstatistics_get_sampletime
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_SignalStatistics::get_SampleTime
 - bdaiface/IBDA_SignalStatistics::get_SampleTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_SignalStatistics.get_SampleTime
---

# IBDA_SignalStatistics::get_SampleTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SampleTime</b> method retrieves the sample time used to measure the signal.

## -parameters

### -param plmsSampleTime [out]

Pointer that receives the sample time.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_sampletime">IBDA_SignalStatistics::put_SampleTime</a>