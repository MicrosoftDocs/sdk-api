---
UID: NF:strmif.IAMTVTuner.put_InputType
title: IAMTVTuner::put_InputType (strmif.h)
author: windows-sdk-content
description: The put_InputType method sets the tuner input type (cable or antenna).
old-location: dshow\iamtvtuner_put_inputtype.htm
tech.root: DirectShow
ms.assetid: d23df6b1-eddc-4c8c-a3c9-400f915e35c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMTVTuner interface [DirectShow],put_InputType method, IAMTVTuner.put_InputType, IAMTVTuner::put_InputType, IAMTVTunerput_InputType, dshow.iamtvtuner_put_inputtype, put_InputType, put_InputType method [DirectShow], put_InputType method [DirectShow],IAMTVTuner interface, strmif/IAMTVTuner::put_InputType
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
 - IAMTVTuner.put_InputType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMTVTuner::put_InputType


## -description



The <code>put_InputType</code> method sets the tuner input type (cable or antenna).




## -parameters




### -param lIndex [in]

Index value that specifies the input pin to be set.


### -param InputType [in]

Value indicating the connection type, as specified in the <a href="https://msdn.microsoft.com/e25ec8e2-6d94-4059-a34e-a9e7887582fb">TunerInputType</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner Interface</a>



<a href="https://msdn.microsoft.com/997d39c5-a1a5-4d2d-8704-9846f149712c">IAMTuner Interface</a>
 

 

