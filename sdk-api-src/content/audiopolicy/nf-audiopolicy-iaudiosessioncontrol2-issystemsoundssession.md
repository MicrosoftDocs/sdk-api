---
UID: NF:audiopolicy.IAudioSessionControl2.IsSystemSoundsSession
title: IAudioSessionControl2::IsSystemSoundsSession (audiopolicy.h)
description: The IsSystemSoundsSession method indicates whether the session is a system sounds session.
helpviewer_keywords: ["IAudioSessionControl2 interface [Core Audio]","IsSystemSoundsSession method","IAudioSessionControl2.IsSystemSoundsSession","IAudioSessionControl2::IsSystemSoundsSession","IsSystemSoundsSession","IsSystemSoundsSession method [Core Audio]","IsSystemSoundsSession method [Core Audio]","IAudioSessionControl2 interface","audiopolicy/IAudioSessionControl2::IsSystemSoundsSession","coreaudio.iaudiosessioncontrol2_issystemsoundssession"]
old-location: coreaudio\iaudiosessioncontrol2_issystemsoundssession.htm
tech.root: CoreAudio
ms.assetid: 9060f89c-83b1-433d-96e3-86ae4b1c7e7c
ms.date: 12/05/2018
ms.keywords: IAudioSessionControl2 interface [Core Audio],IsSystemSoundsSession method, IAudioSessionControl2.IsSystemSoundsSession, IAudioSessionControl2::IsSystemSoundsSession, IsSystemSoundsSession, IsSystemSoundsSession method [Core Audio], IsSystemSoundsSession method [Core Audio],IAudioSessionControl2 interface, audiopolicy/IAudioSessionControl2::IsSystemSoundsSession, coreaudio.iaudiosessioncontrol2_issystemsoundssession
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IAudioSessionControl2::IsSystemSoundsSession
 - audiopolicy/IAudioSessionControl2::IsSystemSoundsSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiopolicy.h
api_name:
 - IAudioSessionControl2.IsSystemSoundsSession
---

# IAudioSessionControl2::IsSystemSoundsSession


## -description

The <b>IsSystemSoundsSession</b> method indicates whether the session is a system sounds session.



## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The session is a system sounds session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The session is not a system sounds session.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2">IAudioSessionControl2</a>
