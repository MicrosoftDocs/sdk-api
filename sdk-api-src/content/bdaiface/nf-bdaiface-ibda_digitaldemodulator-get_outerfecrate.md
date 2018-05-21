---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_OuterFECRate
title: IBDA_DigitalDemodulator::get_OuterFECRate
author: windows-driver-content
description: The get_OuterFECRate method retrieves the outer forward error correction rate for the signal.
old-location: mstv\ibda_digitaldemodulator_get_outerfecrate.htm
old-project: mstv
ms.assetid: 99f6e920-0b2d-4509-9a68-c6404d676b8a
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_OuterFECRate method, IBDA_DigitalDemodulator.get_OuterFECRate, IBDA_DigitalDemodulator::get_OuterFECRate, IBDA_DigitalDemodulatorget_OuterFECRate, bdaiface/IBDA_DigitalDemodulator::get_OuterFECRate, get_OuterFECRate, get_OuterFECRate method [Microsoft TV Technologies], get_OuterFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_outerfecrate
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
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	bdaiface.h
api_name:
-	IBDA_DigitalDemodulator.get_OuterFECRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DigitalDemodulator::get_OuterFECRate


## -description



The <b>get_OuterFECRate</b> method retrieves the outer forward error correction rate for the signal.




## -parameters




### -param pFECRate [out]

Pointer that receives a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556566">BinaryConvolutionCodeRate</a> variable that indicates the rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/13ecd348-dc2b-4e80-9875-927f4ed55c95">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/56fb0c34-8c28-4eff-a1dd-d82c31b0e430">IBDA_DigitalDemodulator::get_InnerFECRate</a>



<a href="https://msdn.microsoft.com/60c35bd1-b971-411b-92bf-bbed41fc984c">IBDA_DigitalDemodulator::put_OuterFECRate</a>
 

 

