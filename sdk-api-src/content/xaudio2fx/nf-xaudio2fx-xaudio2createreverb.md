---
UID: NF:xaudio2fx.XAudio2CreateReverb
title: XAudio2CreateReverb function (xaudio2fx.h)
description: Creates a new reverb audio processing object (APO), and returns a pointer to it.
helpviewer_keywords: ["XAudio2CreateReverb","XAudio2CreateReverb function [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2createreverb","xaudio2fx/XAudio2CreateReverb"]
old-location: xaudio2\xaudio2createreverb.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2CreateReverb(IUnknown@,UINT32)
ms.date: 12/05/2018
ms.keywords: XAudio2CreateReverb, XAudio2CreateReverb function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2createreverb, xaudio2fx/XAudio2CreateReverb
req.header: xaudio2fx.h
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
 - XAudio2CreateReverb
 - xaudio2fx/XAudio2CreateReverb
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.Media.Audio.dll
api_name:
 - XAudio2CreateReverb
---

# XAudio2CreateReverb function


## -description

Creates a new reverb audio processing object (APO), and returns a pointer to it.

## -parameters

### -param ppApo [in, out]

Contains a pointer to the reverb APO that is created.

### -param DEFAULT [in]

Flags that specify the behavior of the APO. The value of this parameter must be 0.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>XAudio2CreateReverb</b> creates an effect performing Princeton Digital Reverb. The XAPO effect library (XAPOFX) includes an alternate reverb effect. Use <a href="/windows/desktop/api/xapofx/nf-xapofx-createfx">CreateFX</a> to create this alternate effect.



The reverb APO supports has the following restrictions:

<ul>
<li>Input audio data must be FLOAT32.

</li>
<li>Framerate must be within XAUDIO2FX_REVERB_MIN_FRAMERATE (20,000 Hz) and XAUDIO2FX_REVERB_MAX_FRAMERATE (48,000 Hz).

</li>
<li>The input and output channels must be one of the following combinations.<ul>
<li>Mono input and mono output

</li>
<li>Mono input and 5.1 output

</li>
<li>Stereo input and stereo output

</li>
<li>Stereo input and 5.1 output</li>
</ul>
</li>
</ul>The reverb APO maintains internal state information between processing samples. You can only use an instance of the APO with one source of audio data at a time. Multiple voices that require reverb effects would each need to create a separate reverb effect with <b>XAudio2CreateReverb</b>.



For information about creating new effects for use with XAudio2, see the <a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>.



<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td>
Because <b>XAudio2CreateReverb</b> calls <b>CoCreateInstance</b> on Windows, the application must have called the <b>CoInitializeEx</b> method before calling <b>XAudio2CreateReverb</b>. <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create">XAudio2Create</a> has the same requirement, which means <b>CoInitializeEx</b> typically will be called long before <b>XAudio2CreateReverb</b> is called.



A typical calling pattern on Windows would be as follows:




```
#ifndef _XBOX
CoInitializeEx(NULL, COINIT_MULTITHREADED);
#endif
IXAudio2* pXAudio2 = NULL;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    return hr;
...
IUnknown * pReverbAPO;
XAudio2CreateReverb(&pReverbAPO);

```


</td>
</tr>
</table>
 

The xaudio2fx.h header defines the <b>AudioReverb</b> class GUID as   a cross-platform audio processing object (XAPO). 


``` syntax
class __declspec(uuid("C2633B16-471B-4498-B8C5-4F0959E2EC09")) AudioReverb;

```

<b>XAudio2CreateReverb</b> returns this object as a pointer to a pointer to <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> in the <i>ppApo</i> parameter. Although you can query the <a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a> and <a href="/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a> interfaces from this <b>IUnknown</b>, you typically never use these interfaces directly. Instead, you use them when you create a voice to add them as part of the effects chain. 

The reverb uses the <a href="/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters">XAUDIO2FX_REVERB_PARAMETERS</a> parameter structure that you access via the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a>. 

> [!NOTE]
> **XAudio2CreateReverb** is an inline function in xaudio2fx.h that calls **CreateAudioReverb** as illustrated in the following code example.

``` syntax
XAUDIO2FX_STDAPI CreateAudioReverb(_Outptr_ IUnknown** ppApo);
__inline HRESULT XAudio2CreateReverb(_Outptr_ IUnknown** ppApo, UINT32 /*Flags*/ DEFAULT(0))
{
    return CreateAudioReverb(ppApo);
}
```

<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--create-an-effect-chain">How to: Create an Effect Chain</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a>



<a href="/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters">XAUDIO2FX_REVERB_PARAMETERS</a>



<a href="/windows/desktop/xaudio2/functions">XAudio2 Functions</a>
