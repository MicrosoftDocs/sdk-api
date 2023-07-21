---
UID: NF:bdaiface.IBDA_SignalStatistics.get_SignalLocked
title: IBDA_SignalStatistics::get_SignalLocked (bdaiface.h)
description: The get_SignalLocked method retrieves a Boolean value indicating whether the signal is locked.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","get_SignalLocked method","IBDA_SignalStatistics.get_SignalLocked","IBDA_SignalStatistics::get_SignalLocked","IBDA_SignalStatisticsget_SignalLocked","bdaiface/IBDA_SignalStatistics::get_SignalLocked","get_SignalLocked","get_SignalLocked method [Microsoft TV Technologies]","get_SignalLocked method [Microsoft TV Technologies]","IBDA_SignalStatistics interface","mstv.ibda_signalstatistics_get_signallocked"]
old-location: mstv\ibda_signalstatistics_get_signallocked.htm
tech.root: mstv
ms.assetid: 2a67ff4b-1abc-43c4-b171-f9af90c5aaf7
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],get_SignalLocked method, IBDA_SignalStatistics.get_SignalLocked, IBDA_SignalStatistics::get_SignalLocked, IBDA_SignalStatisticsget_SignalLocked, bdaiface/IBDA_SignalStatistics::get_SignalLocked, get_SignalLocked, get_SignalLocked method [Microsoft TV Technologies], get_SignalLocked method [Microsoft TV Technologies],IBDA_SignalStatistics interface, mstv.ibda_signalstatistics_get_signallocked
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
 - IBDA_SignalStatistics::get_SignalLocked
 - bdaiface/IBDA_SignalStatistics::get_SignalLocked
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
 - IBDA_SignalStatistics.get_SignalLocked
---

# IBDA_SignalStatistics::get_SignalLocked


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SignalLocked</b> method retrieves a Boolean value indicating whether the signal is locked.

## -parameters

### -param pfLocked [out]

Pointer to a flag indicating whether the signal is locked.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signallocked">IBDA_SignalStatistics::put_SignalLocked</a>