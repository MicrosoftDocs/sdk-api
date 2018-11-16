---
UID: NF:bdaiface.IBDA_DigitalDemodulator.get_SpectralInversion
title: IBDA_DigitalDemodulator::get_SpectralInversion
author: windows-sdk-content
description: The get_SpectralInversion method retrieves the spectral inversion value for the signal.
old-location: mstv\ibda_digitaldemodulator_get_spectralinversion.htm
tech.root: mstv
ms.assetid: eaab17e3-8070-4f70-a31c-cd130edf1a4a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_DigitalDemodulator interface [Microsoft TV Technologies],get_SpectralInversion method, IBDA_DigitalDemodulator.get_SpectralInversion, IBDA_DigitalDemodulator::get_SpectralInversion, IBDA_DigitalDemodulatorget_SpectralInversion, bdaiface/IBDA_DigitalDemodulator::get_SpectralInversion, get_SpectralInversion, get_SpectralInversion method [Microsoft TV Technologies], get_SpectralInversion method [Microsoft TV Technologies],IBDA_DigitalDemodulator interface, mstv.ibda_digitaldemodulator_get_spectralinversion
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
 - IBDA_DigitalDemodulator.get_SpectralInversion
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
- IBDA_DigitalDemodulator.get_SpectralInversion
: 
---

# IBDA_DigitalDemodulator::get_SpectralInversion


## -description



The <b>get_SpectralInversion</b> method retrieves the spectral inversion value for the signal.




## -parameters




### -param pSpectralInversion [out]

Pointer that receives a <a href="https://msdn.microsoft.com/d8781e01-37cc-4c8c-8ff9-61e9c9b95fbd">SpectralInversion</a> variable.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



For more information, see <b>KSPROPERTY_BDA_SPECTRAL_INVERSION</b> in the Windows DDK.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693284(v=VS.85).aspx">IBDA_DigitalDemodulator Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd693306(v=VS.85).aspx">IBDA_DigitalDemodulator::put_SpectralInversion</a>
 

 

