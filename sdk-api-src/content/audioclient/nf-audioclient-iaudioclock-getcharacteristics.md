---
UID: NF:audioclient.IAudioClock.GetCharacteristics
title: IAudioClock::GetCharacteristics (audioclient.h)
description: The GetCharacteristics method is reserved for future use.
helpviewer_keywords: ["GetCharacteristics","GetCharacteristics method [Core Audio]","GetCharacteristics method [Core Audio]","IAudioClock interface","IAudioClock interface [Core Audio]","GetCharacteristics method","IAudioClock.GetCharacteristics","IAudioClock::GetCharacteristics","IAudioClockGetCharacteristics","audioclient/IAudioClock::GetCharacteristics","coreaudio.iaudioclock_getcharacteristics"]
old-location: coreaudio\iaudioclock_getcharacteristics.htm
tech.root: CoreAudio
ms.assetid: a5439a03-9f51-4e51-ab2e-0263de8a3468
ms.date: 12/05/2018
ms.keywords: GetCharacteristics, GetCharacteristics method [Core Audio], GetCharacteristics method [Core Audio],IAudioClock interface, IAudioClock interface [Core Audio],GetCharacteristics method, IAudioClock.GetCharacteristics, IAudioClock::GetCharacteristics, IAudioClockGetCharacteristics, audioclient/IAudioClock::GetCharacteristics, coreaudio.iaudioclock_getcharacteristics
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioClock::GetCharacteristics
 - audioclient/IAudioClock::GetCharacteristics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClock.GetCharacteristics
---

# IAudioClock::GetCharacteristics


## -description

The <b>GetCharacteristics</b> method is reserved for future use.

## -parameters

### -param pdwCharacteristics [out]

Pointer to a <b>DWORD</b> variable into which the method writes a value that indicates the characteristics of the audio clock.

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
Parameter <i>pdwCharacteristics</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclock">IAudioClock Interface</a>