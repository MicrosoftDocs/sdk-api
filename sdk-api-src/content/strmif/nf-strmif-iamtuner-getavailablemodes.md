---
UID: NF:strmif.IAMTuner.GetAvailableModes
title: IAMTuner::GetAvailableModes
author: windows-driver-content
description: The GetAvailableModes method retrieves the tuner's supported modes.
old-location: dshow\iamtuner_getavailablemodes.htm
old-project: DirectShow
ms.assetid: 74025309-2aab-4e0f-95bc-8e6a1e2a5bb4
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetAvailableModes, GetAvailableModes method [DirectShow], GetAvailableModes method [DirectShow],IAMTuner interface, IAMTuner interface [DirectShow],GetAvailableModes method, IAMTuner.GetAvailableModes, IAMTuner::GetAvailableModes, IAMTunerGetAvailableModes, dshow.iamtuner_getavailablemodes, strmif/IAMTuner::GetAvailableModes
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMTuner.GetAvailableModes
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTuner::GetAvailableModes


## -description



The <code>GetAvailableModes</code> method retrieves the tuner's supported modes.




## -parameters




### -param plModes [out]

Pointer to a variable that receives any combination of the values as specified in the <a href="https://msdn.microsoft.com/ce5e6f6d-da79-4a86-abd4-bb28e66d5947">AMTunerModeType</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

