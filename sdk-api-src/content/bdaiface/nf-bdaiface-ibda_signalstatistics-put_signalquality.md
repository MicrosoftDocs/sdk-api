---
UID: NF:bdaiface.IBDA_SignalStatistics.put_SignalQuality
title: IBDA_SignalStatistics::put_SignalQuality
author: windows-sdk-content
description: The put_SignalQuality method specifies the quality of the signal.
old-location: mstv\ibda_signalstatistics_put_signalquality.htm
tech.root: mstv
ms.assetid: e7d73965-4f7e-4330-89f4-2ccbe679ae2a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_SignalStatistics interface [Microsoft TV Technologies],put_SignalQuality method, IBDA_SignalStatistics.put_SignalQuality, IBDA_SignalStatistics::put_SignalQuality, IBDA_SignalStatisticsput_SignalQuality, bdaiface/IBDA_SignalStatistics::put_SignalQuality, mstv.ibda_signalstatistics_put_signalquality, put_SignalQuality, put_SignalQuality method [Microsoft TV Technologies], put_SignalQuality method [Microsoft TV Technologies],IBDA_SignalStatistics interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_SignalStatistics.put_SignalQuality
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_SignalStatistics::put_SignalQuality


## -description



The <b>put_SignalQuality</b> method specifies the quality of the signal.




## -parameters




### -param lPercentQuality [in]

Long integer that specifies the quality of the signal as a percentage. 100 indicates best quality and 0 indicates worst quality.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693432(v=VS.85).aspx">IBDA_SignalStatistics Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693436(v=VS.85).aspx">IBDA_SignalStatistics::get_SignalQuality</a>
 

 

