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

# IBDA_DigitalDemodulator::get_SpectralInversion


## -description



The <b>get_SpectralInversion</b> method retrieves the spectral inversion value for the signal.




## -parameters




### -param pSpectralInversion [out]

Pointer that receives a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568154">SpectralInversion</a> variable.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For more information, see <b>KSPROPERTY_BDA_SPECTRAL_INVERSION</b> in the Windows DDK.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/13ecd348-dc2b-4e80-9875-927f4ed55c95">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/6aabb829-5198-407f-a8f7-f99f87229560">IBDA_DigitalDemodulator::put_SpectralInversion</a>
 

 

