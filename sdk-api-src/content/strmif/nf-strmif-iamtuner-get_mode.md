---
UID: NF:strmif.IAMTuner.get_Mode
title: IAMTuner::get_Mode
author: windows-sdk-content
description: The get_Mode method retrieves the current mode on a multifunction tuner.
old-location: dshow\iamtuner_get_mode.htm
tech.root: DirectShow
ms.assetid: 9a5f4cd8-8fde-4777-b9b6-caa7860b005c
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAMTuner interface [DirectShow],get_Mode method, IAMTuner.get_Mode, IAMTuner::get_Mode, IAMTunerget_Mode, dshow.iamtuner_get_mode, get_Mode, get_Mode method [DirectShow], get_Mode method [DirectShow],IAMTuner interface, strmif/IAMTuner::get_Mode
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
 - IAMTuner.get_Mode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTuner::get_Mode


## -description



The <code>get_Mode</code> method retrieves the current mode on a multifunction tuner.




## -parameters




### -param plMode [out]

Pointer to a variable that receives a flag indicating the current mode setting. The possible values are defined in the <a href="https://msdn.microsoft.com/ce5e6f6d-da79-4a86-abd4-bb28e66d5947">AMTunerModeType</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

