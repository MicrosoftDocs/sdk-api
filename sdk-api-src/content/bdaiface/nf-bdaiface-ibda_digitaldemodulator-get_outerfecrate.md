---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_OuterFECRate
title: IBDA_DigitalDemodulator::get_OuterFECRate
author: windows-sdk-content
description: The get_OuterFECRate method retrieves the outer forward error correction rate for the signal.
old-location: mstv\ibda_digitaldemodulator_get_outerfecrate.htm
tech.root: mstv
ms.assetid: 99f6e920-0b2d-4509-9a68-c6404d676b8a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_OuterFECRate method, IBDA_DigitalDemodulator.get_OuterFECRate, IBDA_DigitalDemodulator::get_OuterFECRate, IBDA_DigitalDemodulatorget_OuterFECRate, bdaiface/IBDA_DigitalDemodulator::get_OuterFECRate, get_OuterFECRate, get_OuterFECRate method [Microsoft TV Technologies], get_OuterFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_outerfecrate
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
 - IBDA_DigitalDemodulator.get_OuterFECRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_DigitalDemodulator::get_OuterFECRate


## -description



The <b>get_OuterFECRate</b> method retrieves the outer forward error correction rate for the signal.




## -parameters




### -param pFECRate [out]

Pointer that receives a <a href="https://msdn.microsoft.com/161c963f-55b2-4a17-a537-47de3326df0e">BinaryConvolutionCodeRate</a> variable that indicates the rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693284(v=VS.85).aspx">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693295(v=VS.85).aspx">IBDA_DigitalDemodulator::get_InnerFECRate</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693305(v=VS.85).aspx">IBDA_DigitalDemodulator::put_OuterFECRate</a>
 

 

