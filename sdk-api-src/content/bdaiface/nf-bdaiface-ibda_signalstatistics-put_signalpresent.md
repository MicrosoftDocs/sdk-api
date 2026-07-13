---
UID: NF:bdaiface.IBDA_SignalStatistics.put_SignalPresent
title: IBDA_SignalStatistics::put_SignalPresent (bdaiface.h)
description: The put_SignalPresent method specifies whether a signal is present.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","put_SignalPresent method","IBDA_SignalStatistics.put_SignalPresent","IBDA_SignalStatistics::put_SignalPresent","IBDA_SignalStatisticsput_SignalPresent","bdaiface/IBDA_SignalStatistics::put_SignalPresent","mstv.ibda_signalstatistics_put_signalpresent","put_SignalPresent","put_SignalPresent method [Microsoft TV Technologies]","put_SignalPresent method [Microsoft TV Technologies]","IBDA_SignalStatistics interface"]
old-location: mstv\ibda_signalstatistics_put_signalpresent.htm
tech.root: mstv
ms.assetid: 9d27dd06-a180-4ee6-bb52-34a8f434ab6a
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],put_SignalPresent method, IBDA_SignalStatistics.put_SignalPresent, IBDA_SignalStatistics::put_SignalPresent, IBDA_SignalStatisticsput_SignalPresent, bdaiface/IBDA_SignalStatistics::put_SignalPresent, mstv.ibda_signalstatistics_put_signalpresent, put_SignalPresent, put_SignalPresent method [Microsoft TV Technologies], put_SignalPresent method [Microsoft TV Technologies],IBDA_SignalStatistics interface
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
 - IBDA_SignalStatistics::put_SignalPresent
 - bdaiface/IBDA_SignalStatistics::put_SignalPresent
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
 - IBDA_SignalStatistics.put_SignalPresent
---

# IBDA_SignalStatistics::put_SignalPresent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_SignalPresent</b> method specifies whether a signal is present.

## -parameters

### -param fPresent [in]

Flag indicating whether the signal is present. <b>TRUE</b> means a signal is present.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_signalpresent">IBDA_SignalStatistics::get_SignalPresent</a>