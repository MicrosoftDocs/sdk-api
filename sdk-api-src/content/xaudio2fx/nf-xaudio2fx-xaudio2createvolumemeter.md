---
UID: NF:xaudio2fx.XAudio2CreateVolumeMeter
title: XAudio2CreateVolumeMeter function (xaudio2fx.h)
description: Creates a new volume meter audio processing object (APO) and returns a pointer to it.
helpviewer_keywords: ["XAudio2CreateVolumeMeter","XAudio2CreateVolumeMeter function [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2createvolumemeter","xaudio2fx/XAudio2CreateVolumeMeter"]
old-location: xaudio2\xaudio2createvolumemeter.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2CreateVolumeMeter(IUnknown@,UINT32)
ms.date: 12/05/2018
ms.keywords: XAudio2CreateVolumeMeter, XAudio2CreateVolumeMeter function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2createvolumemeter, xaudio2fx/XAudio2CreateVolumeMeter
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAudio2CreateVolumeMeter
 - xaudio2fx/XAudio2CreateVolumeMeter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - XAudio2CreateVolumeMeter
---

# XAudio2CreateVolumeMeter function


## -description

Creates a new volume meter audio processing object (APO) and returns a pointer to it.

## -parameters

### -param ppApo [in, out]

Contains the created volume meter APO.

### -param DEFAULT [in]

Flags that specify the behavior of the APO. The value of this parameter must be 0.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For information on creating new effects for use with XAudio2, see the <a href="/windows/desktop/xaudio2/xapo-overview">XAPO Overview</a>.

<table>
<tr>
<th>Windows</th>
</tr>
<tr>
<td>
Because <b>XAudio2CreateVolumeMeter</b> calls <b>CoCreateInstance</b> on Windows, the application must have called the <b>CoInitializeEx</b> method before calling <b>XAudio2CreateVolumeMeter</b>. <a href="/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create">XAudio2Create</a> has the same requirement, which means <b>CoInitializeEx</b> typically will be called long before <b>XAudio2CreateVolumeMeter</b> is called.



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
IUnknown * pVolumeMeterAPO;
XAudio2CreateVolumeMeter(&pVolumeMeterAPO);

```


</td>
</tr>
</table>
 

The xaudio2fx.h header defines the <b>AudioVolumeMeter</b> class GUID as   a cross-platform audio processing object (XAPO). 


``` syntax
class __declspec(uuid("4FC3B166-972A-40CF-BC37-7DB03DB2FBA3")) AudioVolumeMeter;

```

<b>XAudio2CreateVolumeMeter</b> returns this object as a pointer to a pointer to <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> in the <i>ppApo</i> parameter. Although you can query the <a href="/windows/desktop/api/xapo/nn-xapo-ixapo">IXAPO</a> and <a href="/windows/desktop/api/xapo/nn-xapo-ixapoparameters">IXAPOParameters</a> interfaces from this <b>IUnknown</b>, you typically never use these interfaces directly. Instead, you use them when you create a voice to add them as part of the effects chain. 

The volume meter uses the <a href="/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels">XAUDIO2FX_VOLUMEMETER_LEVELS</a> parameter structure that you access via the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-geteffectparameters">IXAudio2Voice::GetEffectParameters</a> method when the XAPO is bound to the audio graph.

<div class="alert"><b>Note</b>  <b>XAudio2CreateVolumeMeter</b> is an inline function in xaudio2fx.h that calls <b>CreateAudioVolumeMeter</b>: 
``` syntax

XAUDIO2FX_STDAPI CreateAudioVolumeMeter(_Outptr_ IUnknown** ppApo);
__inline HRESULT XAudio2CreateVolumeMeter(_Outptr_ IUnknown** ppApo, UINT32 /*Flags*/ DEFAULT(0))
{
    return CreateAudioVolumeMeter(ppApo);
}

```

</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--create-an-effect-chain">How to: Create an Effect Chain</a>



<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters">IXAudio2Voice::SetEffectParameters</a>



<a href="/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels">XAUDIO2FX_VOLUMEMETER_LEVELS</a>



<a href="/windows/desktop/xaudio2/functions">XAudio2 Functions</a>
