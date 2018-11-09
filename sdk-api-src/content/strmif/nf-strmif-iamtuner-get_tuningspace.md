---
UID: NF:strmif.IAMTuner.get_TuningSpace
title: IAMTuner::get_TuningSpace
author: windows-sdk-content
description: The get_TuningSpace method retrieves the tuning space.
old-location: dshow\iamtuner_get_tuningspace.htm
tech.root: DirectShow
ms.assetid: 838451c2-2e0b-4a41-a512-f44283573ee6
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IAMTuner interface [DirectShow],get_TuningSpace method, IAMTuner.get_TuningSpace, IAMTuner::get_TuningSpace, IAMTunerget_TuningSpace, dshow.iamtuner_get_tuningspace, get_TuningSpace, get_TuningSpace method [DirectShow], get_TuningSpace method [DirectShow],IAMTuner interface, strmif/IAMTuner::get_TuningSpace
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
 - IAMTuner.get_TuningSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTuner::get_TuningSpace


## -description



The <code>get_TuningSpace</code> method retrieves the tuning space.




## -parameters




### -param plTuningSpace [out]

Pointer to a variable that receives the current tuning space.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The application defines the value retrieved by this method; it is set through a call to <a href="https://msdn.microsoft.com/fd0c0bc5-2c46-4c5a-8f93-9021f37a6e6a">IAMTuner::put_TuningSpace</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

