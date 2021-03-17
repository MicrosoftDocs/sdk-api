---
UID: NF:audioclient.IAudioClient3.GetCurrentSharedModeEnginePeriod
title: IAudioClient3::GetCurrentSharedModeEnginePeriod (audioclient.h)
description: Returns the current format and periodicity of the audio engine.
helpviewer_keywords: ["GetCurrentSharedModeEnginePeriod","GetCurrentSharedModeEnginePeriod method [Core Audio]","GetCurrentSharedModeEnginePeriod method [Core Audio]","IAudioClient3 interface","IAudioClient3 interface [Core Audio]","GetCurrentSharedModeEnginePeriod method","IAudioClient3.GetCurrentSharedModeEnginePeriod","IAudioClient3::GetCurrentSharedModeEnginePeriod","audioclient/IAudioClient3::GetCurrentSharedModeEnginePeriod","coreaudio.iaudioclient3_getcurrentsharedmodeengineperiod"]
old-location: coreaudio\iaudioclient3_getcurrentsharedmodeengineperiod.htm
tech.root: CoreAudio
ms.assetid: F91E46F5-5D12-4D53-842B-4495CAA3E09E
ms.date: 12/05/2018
ms.keywords: GetCurrentSharedModeEnginePeriod, GetCurrentSharedModeEnginePeriod method [Core Audio], GetCurrentSharedModeEnginePeriod method [Core Audio],IAudioClient3 interface, IAudioClient3 interface [Core Audio],GetCurrentSharedModeEnginePeriod method, IAudioClient3.GetCurrentSharedModeEnginePeriod, IAudioClient3::GetCurrentSharedModeEnginePeriod, audioclient/IAudioClient3::GetCurrentSharedModeEnginePeriod, coreaudio.iaudioclient3_getcurrentsharedmodeengineperiod
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IAudioClient3::GetCurrentSharedModeEnginePeriod
 - audioclient/IAudioClient3::GetCurrentSharedModeEnginePeriod
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioclient.h
api_name:
 - IAudioClient3.GetCurrentSharedModeEnginePeriod
---

# IAudioClient3::GetCurrentSharedModeEnginePeriod


## -description

Returns the current format and periodicity of the audio engine. This method enables audio clients to match the current period of the audio engine.

## -parameters

### -param ppFormat [out]

Type: <b><a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>**</b>

The current device format that is being used by the audio engine.

### -param pCurrentPeriodInFrames [out]

Type: <b>UINT32*</b>

The current period of the audio engine, in audio frames.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -remarks

<div class="alert"><b>Note</b>  The values returned by this method are instantaneous values and may be invalid immediately after the call returns if, for example, another audio client sets the periodicity or format to a different value.</div>
<div> </div>
<div class="alert"><b>Note</b>  The caller is responsible for calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to deallocate the memory of the <b>WAVEFORMATEX</b> structure populated by this method.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient3">IAudioClient3</a>