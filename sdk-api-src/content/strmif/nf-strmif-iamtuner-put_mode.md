---
UID: NF:strmif.IAMTuner.put_Mode
title: IAMTuner::put_Mode
author: windows-sdk-content
description: The put_Mode method sets a multifunction tuner to the specified mode.
old-location: dshow\iamtuner_put_mode.htm
tech.root: DirectShow
ms.assetid: 4c0691fb-e291-43eb-9828-f58474a4334d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAMTuner interface [DirectShow],put_Mode method, IAMTuner.put_Mode, IAMTuner::put_Mode, IAMTunerput_Mode, dshow.iamtuner_put_mode, put_Mode, put_Mode method [DirectShow], put_Mode method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_Mode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner.put_Mode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTuner::put_Mode


## -description



The <code>put_Mode</code> method sets a multifunction tuner to the specified mode.




## -parameters




### -param lMode [in]

Flag indicating which mode to switch to. Possible values are defined in the <a href="https://msdn.microsoft.com/ce5e6f6d-da79-4a86-abd4-bb28e66d5947">AMTunerModeType</a> enumeration.

You can also set the mode to digital TV if the card supports it. To do this, define AMTUNER_MODE_DTV with a value of 0x0010.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>



<a href="https://msdn.microsoft.com/74025309-2aab-4e0f-95bc-8e6a1e2a5bb4">IAMTuner::GetAvailableModes</a>
 

 

