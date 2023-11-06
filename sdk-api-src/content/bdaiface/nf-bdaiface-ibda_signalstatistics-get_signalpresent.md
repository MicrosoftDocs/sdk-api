---
UID: NF:bdaiface.IBDA_SignalStatistics.get_SignalPresent
title: IBDA_SignalStatistics::get_SignalPresent (bdaiface.h)
description: The get_SignalPresent method retrieves a Boolean value indicating whether a signal is present.
helpviewer_keywords: ["IBDA_SignalStatistics interface [Microsoft TV Technologies]","get_SignalPresent method","IBDA_SignalStatistics.get_SignalPresent","IBDA_SignalStatistics::get_SignalPresent","IBDA_SignalStatisticsget_SignalPresent","bdaiface/IBDA_SignalStatistics::get_SignalPresent","get_SignalPresent","get_SignalPresent method [Microsoft TV Technologies]","get_SignalPresent method [Microsoft TV Technologies]","IBDA_SignalStatistics interface","mstv.ibda_signalstatistics_get_signalpresent"]
old-location: mstv\ibda_signalstatistics_get_signalpresent.htm
tech.root: mstv
ms.assetid: 834149e1-50b7-42f6-8fee-a357ed4bc8b8
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],get_SignalPresent method, IBDA_SignalStatistics.get_SignalPresent, IBDA_SignalStatistics::get_SignalPresent, IBDA_SignalStatisticsget_SignalPresent, bdaiface/IBDA_SignalStatistics::get_SignalPresent, get_SignalPresent, get_SignalPresent method [Microsoft TV Technologies], get_SignalPresent method [Microsoft TV Technologies],IBDA_SignalStatistics interface, mstv.ibda_signalstatistics_get_signalpresent
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
 - IBDA_SignalStatistics::get_SignalPresent
 - bdaiface/IBDA_SignalStatistics::get_SignalPresent
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
 - IBDA_SignalStatistics.get_SignalPresent
---

# IBDA_SignalStatistics::get_SignalPresent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SignalPresent</b> method retrieves a Boolean value indicating whether a signal is present.

## -parameters

### -param pfPresent [out]

Pointer to a flag indicating whether a signal is present.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_signalstatistics">IBDA_SignalStatistics Interface</a>



<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signalpresent">IBDA_SignalStatistics::put_SignalPresent</a>