---
UID: NF:devicetopology.IAudioLoudness.GetEnabled
title: IAudioLoudness::GetEnabled (devicetopology.h)
description: The GetEnabled method gets the current state (enabled or disabled) of the loudness control.
helpviewer_keywords: ["GetEnabled","GetEnabled method [Core Audio]","GetEnabled method [Core Audio]","IAudioLoudness interface","IAudioLoudness interface [Core Audio]","GetEnabled method","IAudioLoudness.GetEnabled","IAudioLoudness::GetEnabled","IAudioLoudnessGetEnabled","coreaudio.iaudioloudness_getenabled","devicetopology/IAudioLoudness::GetEnabled"]
old-location: coreaudio\iaudioloudness_getenabled.htm
tech.root: CoreAudio
ms.assetid: 1ce0cd1b-e80f-45dc-b64e-1aa09bb53dbd
ms.date: 12/05/2018
ms.keywords: GetEnabled, GetEnabled method [Core Audio], GetEnabled method [Core Audio],IAudioLoudness interface, IAudioLoudness interface [Core Audio],GetEnabled method, IAudioLoudness.GetEnabled, IAudioLoudness::GetEnabled, IAudioLoudnessGetEnabled, coreaudio.iaudioloudness_getenabled, devicetopology/IAudioLoudness::GetEnabled
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
 - IAudioLoudness::GetEnabled
 - devicetopology/IAudioLoudness::GetEnabled
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
 - IAudioLoudness.GetEnabled
---

# IAudioLoudness::GetEnabled


## -description

The <b>GetEnabled</b> method gets the current state (enabled or disabled) of the loudness control.

## -parameters

### -param pbEnabled [out]

Pointer to a <b>BOOL</b> variable into which the method writes the current loudness state. If the state is <b>TRUE</b>, loudness is enabled. If <b>FALSE</b>, loudness is disabled.

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

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioloudness">IAudioLoudness Interface</a>