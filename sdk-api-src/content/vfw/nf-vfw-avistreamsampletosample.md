---
UID: NF:vfw.AVIStreamSampleToSample
title: AVIStreamSampleToSample macro (vfw.h)
author: windows-sdk-content
description: The AVIStreamSampleToSample macro returns the sample in a stream that occurs at the same time as a sample that occurs in a second stream.
old-location: multimedia\avistreamsampletosample.htm
tech.root: Multimedia
ms.assetid: ed726651-d8f3-4dba-b81d-e283733cabe2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AVIStreamSampleToSample, AVIStreamSampleToSample macro [Windows Multimedia], _win32_AVIStreamSampleToSample, multimedia.avistreamsampletosample, vfw/AVIStreamSampleToSample
ms.topic: macro
f1_keywords: 
 - "vfw/AVIStreamSampleToSample"
dev_langs:
 - c++
req.header: vfw.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVIStreamSampleToSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AVIStreamSampleToSample macro


## -description



The <b>AVIStreamSampleToSample</b> macro returns the sample in a stream that occurs at the same time as a sample that occurs in a second stream.




## -parameters




### -param pavi1

Handle to an open stream that contains the sample that is returned. 


### -param pavi2

Handle to a second stream that contains the reference sample. 


### -param l

Position information of the sample in the stream referenced by pavi2. 


## -remarks



The <b>AVIStreamSampleToSample</b> macro is defined as follows:


```cpp

#define AVIStreamSampleToSample(pavi1, pavi2, lsample) \ 
    AVIStreamTimeToSample(pavi1, AVIStreamSampleToTime \ 
    (pavi2, lsample)) 

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
 

 

