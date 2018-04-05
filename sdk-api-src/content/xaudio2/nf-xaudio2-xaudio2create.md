---
UID: NF:xaudio2.XAudio2Create
title: XAudio2Create function
author: windows-driver-content
description: Creates a new XAudio2 object and returns a pointer to its IXAudio2 interface.
old-location: xaudio2\xaudio2create.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2Create(IXAudio2@,UINT32,XAUDIO2_PROCESSOR)
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: XAudio2Create, XAudio2Create function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2create, xaudio2/XAudio2Create
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Windows.Media.Audio.dll
api_name:
-	XAudio2Create
product: Windows
targetos: Windows
req.lib: Xaudio2.lib
req.dll: Windows.Media.Audio.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# XAudio2Create function


## -description


Creates a new <b>XAudio2</b> object and returns a pointer to its <a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a> interface.


## -parameters




### -param ppXAudio2 [out]

If the operation is successful, returns a pointer to an <a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a> object.


### -param X2DEFAULT

TBD




#### - Flags [in]

Flags that specify the behavior of the <a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a> object. The value of this parameter must be 0.


#### - XAudio2Processor [in]

An <a href="https://msdn.microsoft.com/29E67C0A-36EB-47B2-8708-36EC733D0D37">XAUDIO2_PROCESSOR</a>-typed value that specifies which CPU to use.


<a href="https://msdn.microsoft.com/29E67C0A-36EB-47B2-8708-36EC733D0D37">XAUDIO2_PROCESSOR</a> default value is XAUDIO2_DEFAULT_PROCESSOR.

<div class="alert"><b>Note</b>  Specifying a processor should generally be avoided because it can interfere with the scheduler's ability to schedule threads effectively across processors. Instead, pass the XAUDIO2_DEFAULT_PROCESSOR value (see below).</div>
<div> </div>
The special XAUDIO2_DEFAULT_PROCESSOR value causes XAudio2 to use its default processor.


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes. 




## -remarks



The DirectX SDK versions of XAUDIO2 supported a flag <b>XAUDIO2_DEBUG_ENGINE</b> to select between the release and 'checked' version. This flag is not supported or defined in the Windows 8 version of XAUDIO2.



<div class="alert"><b>Note</b>  No versions of the DirectX SDK contain the xaudio2.lib import library. DirectX SDK versions use COM to create a new <b>XAudio2</b> object.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

<b>Windows Phone 8.1:</b> This API is supported.




## -see-also




<a href="https://msdn.microsoft.com/40f79959-23c9-4513-363b-2f2fc85e4c0a">How to: Build a Basic Audio Processing Graph</a>



<a href="https://msdn.microsoft.com/870a0425-3226-7848-bcc0-0ba7145135cb">XAudio2 Functions</a>
 

 

