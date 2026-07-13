---
UID: NF:bdaiface.IBDA_SignalStatistics.get_SignalQuality
title: IBDA_SignalStatistics::get_SignalQuality (bdaiface.h)
description: The get_SignalQuality method retrieves a value from 1 to 100 indicating the quality of the signal.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","get_SignalQuality method","IBDA_SignalStatistics.get_SignalQuality","IBDA_SignalStatistics::get_SignalQuality","IBDA_SignalStatisticsget_SignalQuality","bdaiface/IBDA_SignalStatistics::get_SignalQuality","get_SignalQuality","get_SignalQuality method [Microsoft TV Technologies]","get_SignalQuality method [Microsoft TV Technologies]","IBDA_SignalStatistics interface","mstv.ibda_signalstatistics_get_signalquality"]
old-location: mstv\ibda_signalstatistics_get_signalquality.htm
tech.root: mstv
ms.assetid: 2472a539-e8ee-4501-b7ab-e7e1fce7cea0
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],get_SignalQuality method, IBDA_SignalStatistics.get_SignalQuality, IBDA_SignalStatistics::get_SignalQuality, IBDA_SignalStatisticsget_SignalQuality, bdaiface/IBDA_SignalStatistics::get_SignalQuality, get_SignalQuality, get_SignalQuality method [Microsoft TV Technologies], get_SignalQuality method [Microsoft TV Technologies],IBDA_SignalStatistics interface, mstv.ibda_signalstatistics_get_signalquality
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
 - IBDA_SignalStatistics::get_SignalQuality
 - bdaiface/IBDA_SignalStatistics::get_SignalQuality
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
 - IBDA_SignalStatistics.get_SignalQuality
---

# IBDA_SignalStatistics::get_SignalQuality


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SignalQuality</b> method retrieves a value from 1 to 100 indicating the quality of the signal.

## -parameters

### -param plPercentQuality [out]

Pointer that receives the value as a percentage. 100 indicates best quality and 0 indicates worst quality.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signalquality">IBDA_SignalStatistics::put_SignalQuality</a>