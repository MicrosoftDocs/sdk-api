---
UID: NF:devicetopology.IAudioMute.GetMute
title: IAudioMute::GetMute (devicetopology.h)
description: The GetMute method gets the current state (enabled or disabled) of the mute control.
helpviewer_keywords: ["GetMute","GetMute method [Core Audio]","GetMute method [Core Audio]","IAudioMute interface","IAudioMute interface [Core Audio]","GetMute method","IAudioMute.GetMute","IAudioMute::GetMute","IAudioMuteGetMute","coreaudio.iaudiomute_getmute","devicetopology/IAudioMute::GetMute"]
old-location: coreaudio\iaudiomute_getmute.htm
tech.root: CoreAudio
ms.assetid: 4b6421d3-f238-46f6-a74a-085a63bf5441
ms.date: 12/05/2018
ms.keywords: GetMute, GetMute method [Core Audio], GetMute method [Core Audio],IAudioMute interface, IAudioMute interface [Core Audio],GetMute method, IAudioMute.GetMute, IAudioMute::GetMute, IAudioMuteGetMute, coreaudio.iaudiomute_getmute, devicetopology/IAudioMute::GetMute
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
 - IAudioMute::GetMute
 - devicetopology/IAudioMute::GetMute
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
 - IAudioMute.GetMute
---

# IAudioMute::GetMute


## -description

The <b>GetMute</b> method gets the current state (enabled or disabled) of the mute control.

## -parameters

### -param pbMuted [out]

Pointer to a <b>BOOL</b> variable into which the method writes the current state of the mute control. If the state is <b>TRUE</b>, muting is enabled. If <b>FALSE</b>, it is disabled.

## -returns

<table>
<tr>
<th>Return code
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>E_POINTER</td>
<td>Pointer <i>pbMuted</i> is <b>NULL</b>.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomute">IAudioMute Interface</a>