---
UID: NF:strmif.IAMTuner.put_TuningSpace
title: IAMTuner::put_TuningSpace
author: windows-driver-content
description: The put_TuningSpace method sets a storage index for regional channel-to-frequency mappings.
old-location: dshow\iamtuner_put_tuningspace.htm
old-project: DirectShow
ms.assetid: fd0c0bc5-2c46-4c5a-8f93-9021f37a6e6a
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMTuner interface [DirectShow],put_TuningSpace method, IAMTuner.put_TuningSpace, IAMTuner::put_TuningSpace, IAMTunerput_TuningSpace, dshow.iamtuner_put_tuningspace, put_TuningSpace, put_TuningSpace method [DirectShow], put_TuningSpace method [DirectShow],IAMTuner interface, strmif/IAMTuner::put_TuningSpace
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
-	IAMTuner.put_TuningSpace
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMTuner::put_TuningSpace


## -description



The <code>put_TuningSpace</code> method sets a storage index for regional channel-to-frequency mappings.




## -parameters




### -param lTuningSpace [in]

Value indicating the current locale.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



As TV tuners move into portable systems, you must retain locale-specific mappings of available channels and their actual frequencies. Formulating different <i>lTuningSpace</i> values for each locale provides a way of switching the channel-to-frequency mappings when moving from region to region.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

