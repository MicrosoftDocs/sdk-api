---
UID: NF:tuner.ITuner.get_SignalStrength
title: ITuner::get_SignalStrength
author: windows-sdk-content
description: The get_SignalStrength method retrieves the Network Provider-specific signal strength metric.
old-location: mstv\ituner_get_signalstrength.htm
tech.root: MSTV
ms.assetid: 3040f56b-2c60-43c8-81b8-5c3538db08db
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_SignalStrength method, ITuner.get_SignalStrength, ITuner::get_SignalStrength, ITunerget_SignalStrength, get_SignalStrength, get_SignalStrength method [Microsoft TV Technologies], get_SignalStrength method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_signalstrength, tuner/ITuner::get_SignalStrength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - tuner.h
api_name:
 - ITuner.get_SignalStrength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITuner::get_SignalStrength


## -description



The <b>get_SignalStrength</b> method retrieves the Network Provider-specific signal strength metric.




## -parameters




### -param Strength

TBD




#### - pStrength [out]

Receives the signal strength.


## -returns



When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The value -1 means can't determine, 0 means not tuned, highest value means best signal. For digital tuners, this also accounts for the FEC bit error rate (BER).




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1bc965a5-6bc9-488a-a2f9-f35d0cfbcccd">ITuner Interface</a>
 

 

