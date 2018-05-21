---
UID: NF:bdaiface.IBDA_DigitalDemodulator.put_InnerFECMethod
title: IBDA_DigitalDemodulator::put_InnerFECMethod
author: windows-driver-content
description: The put_InnerFECMethod method specifies the inner forward error correction method for the signal.
old-location: mstv\ibda_digitaldemodulator_put_innerfecmethod.htm
old-project: mstv
ms.assetid: 618074c0-5139-4373-8bcd-9a8fd90a4ed7
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],put_InnerFECMethod method, IBDA_DigitalDemodulator.put_InnerFECMethod, IBDA_DigitalDemodulator::put_InnerFECMethod, IBDA_DigitalDemodulatorput_InnerFECMethod, bdaiface/IBDA_DigitalDemodulator::put_InnerFECMethod, mstv.ibda_digitaldemodulator_put_innerfecmethod, put_InnerFECMethod, put_InnerFECMethod method [Microsoft TV Technologies], put_InnerFECMethod method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface
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
-	IBDA_DigitalDemodulator.put_InnerFECMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DigitalDemodulator::put_InnerFECMethod


## -description



The <b>put_InnerFECMethod</b> method specifies the inner forward error correction method for the signal.




## -parameters




### -param pFECMethod [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff559594">FECMethod</a> variable that specifies the inner forward error correction method.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/13ecd348-dc2b-4e80-9875-927f4ed55c95">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/a245c9fa-6f1e-4aa6-a5bf-b9707244a9e2">IBDA_DigitalDemodulator::get_InnerFECMethod</a>



<a href="https://msdn.microsoft.com/8ec9c75b-5f71-4a07-8234-8f38b96b962d">IBDA_DigitalDemodulator::put_OuterFECMethod</a>
 

 

