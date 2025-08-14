---
UID: NF:vfw.AVIStreamNextSampleTime
title: AVIStreamNextSampleTime macro (vfw.h)
description: The AVIStreamNextSampleTime macro returns the time that a sample changes to the next sample in the stream. This macro finds the next interesting time in a stream.
helpviewer_keywords: ["AVIStreamNextSampleTime","AVIStreamNextSampleTime macro [Windows Multimedia]","_win32_AVIStreamNextSampleTime","multimedia.avistreamnextsampletime","vfw/AVIStreamNextSampleTime"]
old-location: multimedia\avistreamnextsampletime.htm
tech.root: Multimedia
ms.assetid: 0421f082-9281-4cdb-8b33-2a90c14404dc
ms.date: 07/01/2025
ms.keywords: AVIStreamNextSampleTime, AVIStreamNextSampleTime macro [Windows Multimedia], _win32_AVIStreamNextSampleTime, multimedia.avistreamnextsampletime, vfw/AVIStreamNextSampleTime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIStreamNextSampleTime
 - vfw/AVIStreamNextSampleTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVIStreamNextSampleTime
---

# AVIStreamNextSampleTime macro

## -syntax

```cpp
LONG AVIStreamNextSampleTime(
     pavi,
     t
);
```

## -returns

Type: **LONG**

Returns the time if successful or –1 otherwise.


## -description

The <b>AVIStreamNextSampleTime</b> macro returns the time that a sample changes to the next sample in the stream. This macro finds the next interesting time in a stream.

## -parameters

### -param pavi

Handle to an open stream.

### -param t

Position information of the sample in the stream.

## -remarks

The <b>AVIStreamNextSampleTime</b> macro is defined as follows:


```cpp

#define AVIStreamNextSampleTime(pavi, t) \ 
    AVIStreamSampleToTime(pavi, \ 
    AVIStreamNextSample(pavi, \ 
    AVIStreamTimeToSample(pavi, t))) 

```

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-macros">AVIFile Macros</a>
