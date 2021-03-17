---
UID: NF:devicetopology.IAudioAutoGainControl.GetEnabled
title: IAudioAutoGainControl::GetEnabled (devicetopology.h)
description: The GetEnabled method gets the current state (enabled or disabled) of the AGC.
helpviewer_keywords: ["GetEnabled","GetEnabled method [Core Audio]","GetEnabled method [Core Audio]","IAudioAutoGainControl interface","IAudioAutoGainControl interface [Core Audio]","GetEnabled method","IAudioAutoGainControl.GetEnabled","IAudioAutoGainControl::GetEnabled","IAudioAutoGainControlGetEnabled","coreaudio.iaudioautogaincontrol_getenabled","devicetopology/IAudioAutoGainControl::GetEnabled"]
old-location: coreaudio\iaudioautogaincontrol_getenabled.htm
tech.root: CoreAudio
ms.assetid: 9af85f6e-26b0-45bb-9694-a7578477b456
ms.date: 12/05/2018
ms.keywords: GetEnabled, GetEnabled method [Core Audio], GetEnabled method [Core Audio],IAudioAutoGainControl interface, IAudioAutoGainControl interface [Core Audio],GetEnabled method, IAudioAutoGainControl.GetEnabled, IAudioAutoGainControl::GetEnabled, IAudioAutoGainControlGetEnabled, coreaudio.iaudioautogaincontrol_getenabled, devicetopology/IAudioAutoGainControl::GetEnabled
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IAudioAutoGainControl::GetEnabled
 - devicetopology/IAudioAutoGainControl::GetEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioAutoGainControl.GetEnabled
---

# IAudioAutoGainControl::GetEnabled


## -description

The <b>GetEnabled</b> method gets the current state (enabled or disabled) of the AGC.

## -parameters

### -param pbEnabled [out]

Pointer to a <b>BOOL</b> variable into which the method writes the current AGC state. If the state is <b>TRUE</b>, AGC is enabled. If <b>FALSE</b>, AGC is disabled.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pbEnabled</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

A disabled AGC operates in pass-through mode. In this mode, the audio stream passes through the AGC without modification.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioautogaincontrol">IAudioAutoGainControl Interface</a>