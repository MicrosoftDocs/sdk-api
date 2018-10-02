---
UID: NF:strmif.IAMTVTuner.get_InputType
title: IAMTVTuner::get_InputType
author: windows-sdk-content
description: The get_InputType method retrieves the input type set in IAMTVTuner::put_InputType.
old-location: dshow\iamtvtuner_get_inputtype.htm
tech.root: DirectShow
ms.assetid: 49763cc3-be8b-4620-b99f-af787844c97c
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IAMTVTuner interface [DirectShow],get_InputType method, IAMTVTuner.get_InputType, IAMTVTuner::get_InputType, IAMTVTunerget_InputType, dshow.iamtvtuner_get_inputtype, get_InputType, get_InputType method [DirectShow], get_InputType method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::get_InputType
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
 - IAMTVTuner.get_InputType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMTVTuner::get_InputType


## -description



The <code>get_InputType</code> method retrieves the input type set in <a href="https://msdn.microsoft.com/d23df6b1-eddc-4c8c-a3c9-400f915e35c4">IAMTVTuner::put_InputType</a>.




## -parameters




### -param lIndex [in]

Index value that specifies the input pin that will be set.


### -param pInputType [out]

Pointer to a variable the receives a member of the <a href="https://msdn.microsoft.com/e25ec8e2-6d94-4059-a34e-a9e7887582fb">TunerInputType</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner Interface</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

