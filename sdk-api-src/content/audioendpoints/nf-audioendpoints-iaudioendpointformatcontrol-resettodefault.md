---
UID: NF:audioendpoints.IAudioEndpointFormatControl.ResetToDefault
title: IAudioEndpointFormatControl::ResetToDefault (audioendpoints.h)
description: Resets the format to the default setting provided by the device manufacturer.
helpviewer_keywords: ["IAudioEndpointFormatControl interface [Core Audio]","ResetToDefault method","IAudioEndpointFormatControl.ResetToDefault","IAudioEndpointFormatControl::ResetToDefault","ResetToDefault","ResetToDefault method [Core Audio]","ResetToDefault method [Core Audio]","IAudioEndpointFormatControl interface","audioendpoints/IAudioEndpointFormatControl::ResetToDefault","coreaudio.iaudioendpointformatcontrol_resettodefault"]
old-location: coreaudio\iaudioendpointformatcontrol_resettodefault.htm
tech.root: CoreAudio
ms.assetid: EAE5206D-8BDF-4016-A0E6-D56D0F6B3566
ms.date: 12/05/2018
ms.keywords: IAudioEndpointFormatControl interface [Core Audio],ResetToDefault method, IAudioEndpointFormatControl.ResetToDefault, IAudioEndpointFormatControl::ResetToDefault, ResetToDefault, ResetToDefault method [Core Audio], ResetToDefault method [Core Audio],IAudioEndpointFormatControl interface, audioendpoints/IAudioEndpointFormatControl::ResetToDefault, coreaudio.iaudioendpointformatcontrol_resettodefault
req.header: audioendpoints.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IAudioEndpointFormatControl::ResetToDefault
 - audioendpoints/IAudioEndpointFormatControl::ResetToDefault
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AudioEndpoints.h
api_name:
 - IAudioEndpointFormatControl.ResetToDefault
---

# IAudioEndpointFormatControl::ResetToDefault


## -description

Resets the format to the default setting provided by the device manufacturer.

## -parameters

### -param ResetFlags [in]

Allows the application to specify which formats are reset.  If
                      no flags are set, then this method reevaluates both the endpoint's 
    device format and mix format and sets them to their default values.

ENDPOINT_FORMAT_RESET_MIX_ONLY: Only reset the mix format.  The endpoint's device
    format will not be reset if this flag is set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/audioendpoints/nn-audioendpoints-iaudioendpointformatcontrol">IAudioEndpointFormatControl</a>