---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_InnerFECRate
title: IBDA_DigitalDemodulator::get_InnerFECRate
author: windows-sdk-content
description: The get_InnerFECRate method retrieves the inner forward error correction rate being used on the signal.
old-location: mstv\ibda_digitaldemodulator_get_innerfecrate.htm
old-project: mstv
ms.assetid: 56fb0c34-8c28-4eff-a1dd-d82c31b0e430
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_InnerFECRate method, IBDA_DigitalDemodulator.get_InnerFECRate, IBDA_DigitalDemodulator::get_InnerFECRate, IBDA_DigitalDemodulatorget_InnerFECRate, bdaiface/IBDA_DigitalDemodulator::get_InnerFECRate, get_InnerFECRate, get_InnerFECRate method [Microsoft TV Technologies], get_InnerFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_innerfecrate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdaiface.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UICloseReasonType
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
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DigitalDemodulator::get_InnerFECRate


## -description



The <b>get_InnerFECRate</b> method retrieves the inner forward error correction rate being used on the signal.




## -parameters




### -param pFECRate [out]

Pointer that receives a <a href="https://msdn.microsoft.com/161c963f-55b2-4a17-a537-47de3326df0e">BinaryConvolutionCodeRate</a> variable that indicates the rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/13ecd348-dc2b-4e80-9875-927f4ed55c95">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/99f6e920-0b2d-4509-9a68-c6404d676b8a">IBDA_DigitalDemodulator::get_OuterFECRate</a>



<a href="https://msdn.microsoft.com/e87dbce2-6970-45f6-b08c-bddebeb4d1ca">IBDA_DigitalDemodulator::put_InnerFECRate</a>
 

 

