---
UID: NF:audioengineendpoint.IAudioLfxControl.GetLocalEffectsState
title: IAudioLfxControl::GetLocalEffectsState (audioengineendpoint.h)
description: The GetLocalEffectsState method retrieves the local effects state that is currently applied to the offloaded audio stream.
helpviewer_keywords: ["GetLocalEffectsState","GetLocalEffectsState method [Core Audio]","GetLocalEffectsState method [Core Audio]","IAudioLfxControl interface","IAudioLfxControl interface [Core Audio]","GetLocalEffectsState method","IAudioLfxControl.GetLocalEffectsState","IAudioLfxControl::GetLocalEffectsState","audioengineendpoint/IAudioLfxControl::GetLocalEffectsState","coreaudio.iaudiolfxcontrol_getlocaleffectsstate"]
old-location: coreaudio\iaudiolfxcontrol_getlocaleffectsstate.htm
tech.root: CoreAudio
ms.assetid: 33426EAC-13E6-4AF2-9D01-7C3057EB8104
ms.date: 12/05/2018
ms.keywords: GetLocalEffectsState, GetLocalEffectsState method [Core Audio], GetLocalEffectsState method [Core Audio],IAudioLfxControl interface, IAudioLfxControl interface [Core Audio],GetLocalEffectsState method, IAudioLfxControl.GetLocalEffectsState, IAudioLfxControl::GetLocalEffectsState, audioengineendpoint/IAudioLfxControl::GetLocalEffectsState, coreaudio.iaudiolfxcontrol_getlocaleffectsstate
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IAudioLfxControl::GetLocalEffectsState
 - audioengineendpoint/IAudioLfxControl::GetLocalEffectsState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioLfxControl.GetLocalEffectsState
---

# IAudioLfxControl::GetLocalEffectsState


## -description

The <b>GetLocalEffectsState</b> method retrieves the local effects state that is currently applied to the offloaded audio stream.

## -parameters

### -param pbEnabled [out]

A pointer to the Boolean variable that indicates the state of the local effects that have been applied to the offloaded audio stream. A value of <b>TRUE</b> indicates that local effects have been enabled and applied to the stream. A value of <b>FALSE</b> indicates that local effects have been disabled.

## -returns

The <b>GetLocalEffectsState</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiolfxcontrol">IAudioLfxControl</a>