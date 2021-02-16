---
UID: NF:devicetopology.IAudioMute.SetMute
title: IAudioMute::SetMute (devicetopology.h)
description: The SetMute method enables or disables the mute control.
helpviewer_keywords: ["IAudioMute interface [Core Audio]","SetMute method","IAudioMute.SetMute","IAudioMute::SetMute","IAudioMuteSetMute","SetMute","SetMute method [Core Audio]","SetMute method [Core Audio]","IAudioMute interface","coreaudio.iaudiomute_setmute","devicetopology/IAudioMute::SetMute"]
old-location: coreaudio\iaudiomute_setmute.htm
tech.root: CoreAudio
ms.assetid: e99cb894-b39e-42ec-be8f-dc3fa6e7abcd
ms.date: 12/05/2018
ms.keywords: IAudioMute interface [Core Audio],SetMute method, IAudioMute.SetMute, IAudioMute::SetMute, IAudioMuteSetMute, SetMute, SetMute method [Core Audio], SetMute method [Core Audio],IAudioMute interface, coreaudio.iaudiomute_setmute, devicetopology/IAudioMute::SetMute
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
 - IAudioMute::SetMute
 - devicetopology/IAudioMute::SetMute
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
 - IAudioMute.SetMute
---

# IAudioMute::SetMute


## -description

The <b>SetMute</b> method enables or disables the mute control.

## -parameters

### -param bMuted [in]

The new muting state. If <i>bMuted</i> is <b>TRUE</b> (nonzero), the method enables muting. If <b>FALSE</b>, the method disables muting.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetMute</b> call changes the state of the mute control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudiomute">IAudioMute Interface</a>