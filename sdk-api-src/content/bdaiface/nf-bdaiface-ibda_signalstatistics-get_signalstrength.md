---
UID: NF:bdaiface.IBDA_SignalStatistics.get_SignalStrength
title: IBDA_SignalStatistics::get_SignalStrength (bdaiface.h)
description: The get_SignalStrength method retrieves a value that indicates the strength of the signal in decibels.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","get_SignalStrength method","IBDA_SignalStatistics.get_SignalStrength","IBDA_SignalStatistics::get_SignalStrength","IBDA_SignalStatisticsget_SignalStrength","bdaiface/IBDA_SignalStatistics::get_SignalStrength","get_SignalStrength","get_SignalStrength method [Microsoft TV Technologies]","get_SignalStrength method [Microsoft TV Technologies]","IBDA_SignalStatistics interface","mstv.ibda_signalstatistics_get_signalstrength"]
old-location: mstv\ibda_signalstatistics_get_signalstrength.htm
tech.root: mstv
ms.assetid: f4830da1-1031-456e-8f3f-eb15f5366942
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],get_SignalStrength method, IBDA_SignalStatistics.get_SignalStrength, IBDA_SignalStatistics::get_SignalStrength, IBDA_SignalStatisticsget_SignalStrength, bdaiface/IBDA_SignalStatistics::get_SignalStrength, get_SignalStrength, get_SignalStrength method [Microsoft TV Technologies], get_SignalStrength method [Microsoft TV Technologies],IBDA_SignalStatistics interface, mstv.ibda_signalstatistics_get_signalstrength
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
 - IBDA_SignalStatistics::get_SignalStrength
 - bdaiface/IBDA_SignalStatistics::get_SignalStrength
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
 - IBDA_SignalStatistics.get_SignalStrength
---

# IBDA_SignalStatistics::get_SignalStrength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SignalStrength</b> method retrieves a value that indicates the strength of the signal in decibels.

## -parameters

### -param plDbStrength [out]

Pointer that receives the signal strength value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signalstrength">IBDA_SignalStatistics::put_SignalStrength</a>