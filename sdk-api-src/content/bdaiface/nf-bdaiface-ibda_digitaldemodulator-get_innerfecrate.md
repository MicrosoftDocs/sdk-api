---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_InnerFECRate
title: IBDA_DigitalDemodulator::get_InnerFECRate
author: windows-sdk-content
description: The get_InnerFECRate method retrieves the inner forward error correction rate being used on the signal.
old-location: mstv\ibda_digitaldemodulator_get_innerfecrate.htm
tech.root: mstv
ms.assetid: 56fb0c34-8c28-4eff-a1dd-d82c31b0e430
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_InnerFECRate method, IBDA_DigitalDemodulator.get_InnerFECRate, IBDA_DigitalDemodulator::get_InnerFECRate, IBDA_DigitalDemodulatorget_InnerFECRate, bdaiface/IBDA_DigitalDemodulator::get_InnerFECRate, get_InnerFECRate, get_InnerFECRate method [Microsoft TV Technologies], get_InnerFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_innerfecrate
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
 - IBDA_DigitalDemodulator.get_InnerFECRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_DigitalDemodulator::get_InnerFECRate


## -description



The <b>get_InnerFECRate</b> method retrieves the inner forward error correction rate being used on the signal.




## -parameters




### -param pFECRate [out]

Pointer that receives a <a href="https://msdn.microsoft.com/en-us/library/Dd693025(v=VS.85).aspx">BinaryConvolutionCodeRate</a> variable that indicates the rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693284(v=VS.85).aspx">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693298(v=VS.85).aspx">IBDA_DigitalDemodulator::get_OuterFECRate</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693302(v=VS.85).aspx">IBDA_DigitalDemodulator::put_InnerFECRate</a>
 

 

