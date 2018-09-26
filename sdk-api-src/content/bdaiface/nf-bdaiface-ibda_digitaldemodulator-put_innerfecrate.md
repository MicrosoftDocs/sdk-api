---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_InnerFECRate
title: IBDA_DigitalDemodulator::put_InnerFECRate
author: windows-sdk-content
description: The put_InnerFECRate method specifies the inner forward error correction rate.
old-location: mstv\ibda_digitaldemodulator_put_innerfecrate.htm
tech.root: MSTV
ms.assetid: e87dbce2-6970-45f6-b08c-bddebeb4d1ca
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_InnerFECRate method, IBDA_DigitalDemodulator.put_InnerFECRate, IBDA_DigitalDemodulator::put_InnerFECRate, IBDA_DigitalDemodulatorput_InnerFECRate, bdaiface/IBDA_DigitalDemodulator::put_InnerFECRate, mstv.ibda_digitaldemodulator_put_innerfecrate, put_InnerFECRate, put_InnerFECRate method [Microsoft TV Technologies], put_InnerFECRate method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
 - IBDA_DigitalDemodulator.put_InnerFECRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_DigitalDemodulator::put_InnerFECRate


## -description



The <b>put_InnerFECRate</b> method specifies the inner forward error correction rate.




## -parameters




### -param pFECRate [in]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Dd693025(v=VS.85).aspx">BinaryConvolutionCodeRate</a> variable that specifies the inner FEC rate.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693284(v=VS.85).aspx">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693295(v=VS.85).aspx">IBDA_DigitalDemodulator::get_InnerFECRate</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693305(v=VS.85).aspx">IBDA_DigitalDemodulator::put_OuterFECRate</a>
 

 

