---
UID: NF:devicetopology.IAudioLoudness.SetEnabled
title: IAudioLoudness::SetEnabled (devicetopology.h)
description: The SetEnabled method enables or disables the loudness control.
helpviewer_keywords: ["IAudioLoudness interface [Core Audio]","SetEnabled method","IAudioLoudness.SetEnabled","IAudioLoudness::SetEnabled","IAudioLoudnessSetEnabled","SetEnabled","SetEnabled method [Core Audio]","SetEnabled method [Core Audio]","IAudioLoudness interface","coreaudio.iaudioloudness_setenabled","devicetopology/IAudioLoudness::SetEnabled"]
old-location: coreaudio\iaudioloudness_setenabled.htm
tech.root: CoreAudio
ms.assetid: a9102346-e853-40ae-ae10-a3e864ec5f17
ms.date: 12/05/2018
ms.keywords: IAudioLoudness interface [Core Audio],SetEnabled method, IAudioLoudness.SetEnabled, IAudioLoudness::SetEnabled, IAudioLoudnessSetEnabled, SetEnabled, SetEnabled method [Core Audio], SetEnabled method [Core Audio],IAudioLoudness interface, coreaudio.iaudioloudness_setenabled, devicetopology/IAudioLoudness::SetEnabled
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
 - IAudioLoudness::SetEnabled
 - devicetopology/IAudioLoudness::SetEnabled
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
 - IAudioLoudness.SetEnabled
---

# IAudioLoudness::SetEnabled


## -description

The <b>SetEnabled</b> method enables or disables the loudness control.

## -parameters

### -param bEnable [in]

The new loudness state. If <i>bEnable</i> is <b>TRUE</b> (nonzero), the method enables loudness. If <b>FALSE</b>, it disables loudness.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetEnabled</b> call changes the state of the loudness control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioloudness">IAudioLoudness Interface</a>