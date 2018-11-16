---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_OuterFECRate
title: IBDA_DigitalDemodulator::put_OuterFECRate
author: windows-sdk-content
description: The put_OuterFECRate method specifies the outer forward error correction rate for the signal.
old-location: mstv\ibda_digitaldemodulator_put_outerfecrate.htm
tech.root: mstv
ms.assetid: 60c35bd1-b971-411b-92bf-bbed41fc984c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_OuterFECRate method, IBDA_DigitalDemodulator.put_OuterFECRate, IBDA_DigitalDemodulator::put_OuterFECRate, IBDA_DigitalDemodulatorput_OuterFECRate, bdaiface/IBDA_DigitalDemodulator::put_OuterFECRate, mstv.ibda_digitaldemodulator_put_outerfecrate, put_OuterFECRate, put_OuterFECRate method [Microsoft TV Technologies], put_OuterFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator.put_OuterFECRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- bdaiface.h
: 
- IBDA_DigitalDemodulator.put_OuterFECRate
: 
---

# IBDA_DigitalDemodulator::put_OuterFECRate


## -description



The <b>put_OuterFECRate</b> method specifies the outer forward error correction rate for the signal.




## -parameters




### -param pFECRate [in]

Pointer to a <a href="https://msdn.microsoft.com/161c963f-55b2-4a17-a537-47de3326df0e">BinaryConvolutionCodeRate</a> variable that specifies the FEC rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/13ecd348-dc2b-4e80-9875-927f4ed55c95">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/99f6e920-0b2d-4509-9a68-c6404d676b8a">IBDA_DigitalDemodulator::get_OuterFECRate</a>



<a href="https://msdn.microsoft.com/e87dbce2-6970-45f6-b08c-bddebeb4d1ca">IBDA_DigitalDemodulator::put_InnerFECRate</a>
 

 

