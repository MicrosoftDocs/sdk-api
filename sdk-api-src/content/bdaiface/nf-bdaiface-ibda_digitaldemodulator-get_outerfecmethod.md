---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IBDA_DigitalDemodulator::get_OuterFECMethod


## -description



The <b>get_OuterFECMethod</b> method retrieves the outer forward error correction method for the signal .




## -parameters




### -param pFECMethod [out]

Pointer that receives an <a href="https://msdn.microsoft.com/library/windows/hardware/ff559594">FECMethod</a> variable that indicates the FEC method.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/13ecd348-dc2b-4e80-9875-927f4ed55c95">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/a245c9fa-6f1e-4aa6-a5bf-b9707244a9e2">IBDA_DigitalDemodulator::get_InnerFECMethod</a>



<a href="https://msdn.microsoft.com/8ec9c75b-5f71-4a07-8234-8f38b96b962d">IBDA_DigitalDemodulator::put_OuterFECMethod</a>
 

 

