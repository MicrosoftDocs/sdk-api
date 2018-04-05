---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_SpectralInversion
title: IBDA_DigitalDemodulator::get_SpectralInversion method
author: windows-driver-content
description: The get_SpectralInversion method retrieves the spectral inversion value for the signal.
old-location: mstv\ibda_digitaldemodulator_get_spectralinversion.htm
old-project: mstv
ms.assetid: eaab17e3-8070-4f70-a31c-cd130edf1a4a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IBDA_DigitalDemodulator, IBDA_DigitalDemodulator interface [Microsoft TV Technologies], get_SpectralInversion method, IBDA_DigitalDemodulator::get_SpectralInversion, IBDA_DigitalDemodulatorget_SpectralInversion, bdaiface/IBDA_DigitalDemodulator::get_SpectralInversion, get_SpectralInversion method [Microsoft TV Technologies], get_SpectralInversion method [Microsoft TV Technologies], IBDA_DigitalDemodulator interface, get_SpectralInversion,IBDA_DigitalDemodulator.get_SpectralInversion, mstv.ibda_digitaldemodulator_get_spectralinversion
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
-	IBDA_DigitalDemodulator.get_SpectralInversion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_DigitalDemodulator::get_SpectralInversion method


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
 

 

