---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_OuterFECMethod
title: IBDA_DigitalDemodulator::get_OuterFECMethod
author: windows-sdk-content
description: The get_OuterFECMethod method retrieves the outer forward error correction method for the signal .
old-location: mstv\ibda_digitaldemodulator_get_outerfecmethod.htm
tech.root: mstv
ms.assetid: 6fbedcba-4b76-4cf0-8fa1-c71140d49643
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_OuterFECMethod method, IBDA_DigitalDemodulator.get_OuterFECMethod, IBDA_DigitalDemodulator::get_OuterFECMethod, IBDA_DigitalDemodulatorget_OuterFECMethod, bdaiface/IBDA_DigitalDemodulator::get_OuterFECMethod, get_OuterFECMethod, get_OuterFECMethod method [Microsoft TV Technologies], get_OuterFECMethod method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_outerfecmethod
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
 - IBDA_DigitalDemodulator.get_OuterFECMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_DigitalDemodulator::get_OuterFECMethod


## -description



The <b>get_OuterFECMethod</b> method retrieves the outer forward error correction method for the signal .




## -parameters




### -param pFECMethod [out]

Pointer that receives an <a href="https://msdn.microsoft.com/en-us/library/Dd693082(v=VS.85).aspx">FECMethod</a> variable that indicates the FEC method.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693284(v=VS.85).aspx">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693294(v=VS.85).aspx">IBDA_DigitalDemodulator::get_InnerFECMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693304(v=VS.85).aspx">IBDA_DigitalDemodulator::put_OuterFECMethod</a>
 

 

