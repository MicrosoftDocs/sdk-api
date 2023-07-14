---
UID: NF:bdaiface.IBDA_SignalStatistics.put_SignalStrength
title: IBDA_SignalStatistics::put_SignalStrength (bdaiface.h)
description: The put_SignalStrength method specifies the strength of the signal in decibels.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","put_SignalStrength method","IBDA_SignalStatistics.put_SignalStrength","IBDA_SignalStatistics::put_SignalStrength","IBDA_SignalStatisticsput_SignalStrength","bdaiface/IBDA_SignalStatistics::put_SignalStrength","mstv.ibda_signalstatistics_put_signalstrength","put_SignalStrength","put_SignalStrength method [Microsoft TV Technologies]","put_SignalStrength method [Microsoft TV Technologies]","IBDA_SignalStatistics interface"]
old-location: mstv\ibda_signalstatistics_put_signalstrength.htm
tech.root: mstv
ms.assetid: 3a1f11b7-09f4-430a-8976-81f15ea22b1a
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],put_SignalStrength method, IBDA_SignalStatistics.put_SignalStrength, IBDA_SignalStatistics::put_SignalStrength, IBDA_SignalStatisticsput_SignalStrength, bdaiface/IBDA_SignalStatistics::put_SignalStrength, mstv.ibda_signalstatistics_put_signalstrength, put_SignalStrength, put_SignalStrength method [Microsoft TV Technologies], put_SignalStrength method [Microsoft TV Technologies],IBDA_SignalStatistics interface
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
 - IBDA_SignalStatistics::put_SignalStrength
 - bdaiface/IBDA_SignalStatistics::put_SignalStrength
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
 - IBDA_SignalStatistics.put_SignalStrength
---

# IBDA_SignalStatistics::put_SignalStrength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SignalStrength</b> method specifies the strength of the signal in decibels.

## -parameters

### -param lDbStrength [in]

Long integer that specifies the db strength.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_signalstrength">IBDA_SignalStatistics::get_SignalStrength</a>