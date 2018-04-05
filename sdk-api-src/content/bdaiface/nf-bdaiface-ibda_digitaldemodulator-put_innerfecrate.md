---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_InnerFECRate
title: IBDA_DigitalDemodulator::put_InnerFECRate method
author: windows-driver-content
description: The put_InnerFECRate method specifies the inner forward error correction rate.
old-location: mstv\ibda_digitaldemodulator_put_innerfecrate.htm
old-project: mstv
ms.assetid: e87dbce2-6970-45f6-b08c-bddebeb4d1ca
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IBDA_DigitalDemodulator, IBDA_DigitalDemodulator interface [Microsoft TV Technologies], put_InnerFECRate method, IBDA_DigitalDemodulator::put_InnerFECRate, IBDA_DigitalDemodulatorput_InnerFECRate, bdaiface/IBDA_DigitalDemodulator::put_InnerFECRate, mstv.ibda_digitaldemodulator_put_innerfecrate, put_InnerFECRate method [Microsoft TV Technologies], put_InnerFECRate method [Microsoft TV Technologies], IBDA_DigitalDemodulator interface, put_InnerFECRate,IBDA_DigitalDemodulator.put_InnerFECRate
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
-	IBDA_DigitalDemodulator.put_InnerFECRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DigitalDemodulator::put_InnerFECRate method


## -description



The <b>put_InnerFECRate</b> method specifies the inner forward error correction rate.




## -parameters




### -param pFECRate [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556566">BinaryConvolutionCodeRate</a> variable that specifies the inner FEC rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/13ecd348-dc2b-4e80-9875-927f4ed55c95">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/56fb0c34-8c28-4eff-a1dd-d82c31b0e430">IBDA_DigitalDemodulator::get_InnerFECRate</a>



<a href="https://msdn.microsoft.com/60c35bd1-b971-411b-92bf-bbed41fc984c">IBDA_DigitalDemodulator::put_OuterFECRate</a>
 

 

