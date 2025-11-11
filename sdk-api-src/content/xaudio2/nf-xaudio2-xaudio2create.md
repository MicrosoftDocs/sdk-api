---
UID: NF:xaudio2.XAudio2Create
title: XAudio2Create function (xaudio2.h)
description: Creates a new XAudio2 object and returns a pointer to its IXAudio2 interface.
helpviewer_keywords: ["XAudio2Create","XAudio2Create function [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2create","xaudio2/XAudio2Create"]
old-location: xaudio2\xaudio2create.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2Create(IXAudio2@,UINT32,XAUDIO2_PROCESSOR)
ms.date: 12/05/2018
ms.keywords: XAudio2Create, XAudio2Create function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2create, xaudio2/XAudio2Create
req.header: xaudio2.h
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
req.lib: Xaudio2.lib
req.dll: Windows.Media.Audio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAudio2Create
 - xaudio2/XAudio2Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.Media.Audio.dll
 - xaudio2_8.dll
 - xaudio2_9.dll
api_name:
 - XAudio2Create
---

# XAudio2Create function


## -description

Creates a new <b>XAudio2</b> object and returns a pointer to its <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a> interface.

## -parameters

### -param ppXAudio2 [out]

If the operation is successful, returns a pointer to an <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a> object.

### -param Flags [in]

Flags that specify the behavior of the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2">IXAudio2</a> object. The value of this parameter must be 0.

### -param XAudio2Processor [in]

An <a href="/windows/desktop/xaudio2/uint32-xaudio2-processor">XAUDIO2_PROCESSOR</a>-typed value that specifies which CPU to use. If multiple bits are specified, the system will create a separate worker thread for each processor.


<a href="/windows/desktop/xaudio2/uint32-xaudio2-processor">XAUDIO2_PROCESSOR</a> default value is XAUDIO2_DEFAULT_PROCESSOR.

<div class="alert"><b>Warning</b> If you specify <a href="/windows/desktop/xaudio2/uint32-xaudio2-processor">XAUDIO2_ANY_PROCESSOR</a>, the system will use all of the device's processors and, as noted above, create a worker thread for each processor.</div>
<div> </div>


<div class="alert"><b>Note</b>  Specifying a processor should generally be avoided because it can interfere with the scheduler's ability to schedule threads effectively across processors. Instead, pass the XAUDIO2_DEFAULT_PROCESSOR value (see below).</div>
<div> </div>
The special XAUDIO2_DEFAULT_PROCESSOR value causes XAudio2 to use its default processor.

## -returns

Returns S_OK if successful, an error code otherwise. See <a href="/windows/desktop/xaudio2/xaudio2-error-codes">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.

## -remarks

The DirectX SDK versions of XAUDIO2 supported a flag <b>XAUDIO2_DEBUG_ENGINE</b> to select between the release and 'checked' version. This flag is not supported or defined in the Windows 8 version of XAUDIO2.



<div class="alert"><b>Note</b>  No versions of the DirectX SDK contain the xaudio2.lib import library. DirectX SDK versions use COM to create a new <b>XAudio2</b> object.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

<b>Windows Phone 8.1:</b> This API is supported.

## -see-also

<a href="/windows/desktop/xaudio2/how-to--build-a-basic-audio-processing-graph">How to: Build a Basic Audio Processing Graph</a>



<a href="/windows/desktop/xaudio2/functions">XAudio2 Functions</a>
