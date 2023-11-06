---
UID: NF:bdaiface.IBDA_SignalStatistics.put_SignalLocked
title: IBDA_SignalStatistics::put_SignalLocked (bdaiface.h)
description: The put_SignalLocked method specifies whether the signal is locked.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","put_SignalLocked method","IBDA_SignalStatistics.put_SignalLocked","IBDA_SignalStatistics::put_SignalLocked","IBDA_SignalStatisticsput_SignalLocked","bdaiface/IBDA_SignalStatistics::put_SignalLocked","mstv.ibda_signalstatistics_put_signallocked","put_SignalLocked","put_SignalLocked method [Microsoft TV Technologies]","put_SignalLocked method [Microsoft TV Technologies]","IBDA_SignalStatistics interface"]
old-location: mstv\ibda_signalstatistics_put_signallocked.htm
tech.root: mstv
ms.assetid: 26e4053f-7e43-464d-8ea1-076f741d5b63
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],put_SignalLocked method, IBDA_SignalStatistics.put_SignalLocked, IBDA_SignalStatistics::put_SignalLocked, IBDA_SignalStatisticsput_SignalLocked, bdaiface/IBDA_SignalStatistics::put_SignalLocked, mstv.ibda_signalstatistics_put_signallocked, put_SignalLocked, put_SignalLocked method [Microsoft TV Technologies], put_SignalLocked method [Microsoft TV Technologies],IBDA_SignalStatistics interface
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
 - IBDA_SignalStatistics::put_SignalLocked
 - bdaiface/IBDA_SignalStatistics::put_SignalLocked
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
 - IBDA_SignalStatistics.put_SignalLocked
---

# IBDA_SignalStatistics::put_SignalLocked


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SignalLocked</b> method specifies whether the signal is locked.

## -parameters

### -param fLocked [in]

Flag that indicates whether to lock the signal.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_signallocked">IBDA_SignalStatistics::get_SignalLocked</a>