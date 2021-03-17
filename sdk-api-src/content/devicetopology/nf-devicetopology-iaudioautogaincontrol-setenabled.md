---
UID: NF:devicetopology.IAudioAutoGainControl.SetEnabled
title: IAudioAutoGainControl::SetEnabled (devicetopology.h)
description: The SetEnabled method enables or disables the AGC.
helpviewer_keywords: ["IAudioAutoGainControl interface [Core Audio]","SetEnabled method","IAudioAutoGainControl.SetEnabled","IAudioAutoGainControl::SetEnabled","IAudioAutoGainControlSetEnabled","SetEnabled","SetEnabled method [Core Audio]","SetEnabled method [Core Audio]","IAudioAutoGainControl interface","coreaudio.iaudioautogaincontrol_setenabled","devicetopology/IAudioAutoGainControl::SetEnabled"]
old-location: coreaudio\iaudioautogaincontrol_setenabled.htm
tech.root: CoreAudio
ms.assetid: 05bf3b59-20e9-4bb0-931b-b6f28676cb5f
ms.date: 12/05/2018
ms.keywords: IAudioAutoGainControl interface [Core Audio],SetEnabled method, IAudioAutoGainControl.SetEnabled, IAudioAutoGainControl::SetEnabled, IAudioAutoGainControlSetEnabled, SetEnabled, SetEnabled method [Core Audio], SetEnabled method [Core Audio],IAudioAutoGainControl interface, coreaudio.iaudioautogaincontrol_setenabled, devicetopology/IAudioAutoGainControl::SetEnabled
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
 - IAudioAutoGainControl::SetEnabled
 - devicetopology/IAudioAutoGainControl::SetEnabled
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
 - IAudioAutoGainControl.SetEnabled
---

# IAudioAutoGainControl::SetEnabled


## -description

The <b>SetEnabled</b> method enables or disables the AGC.

## -parameters

### -param bEnable [in]

The new AGC state. If this parameter is <b>TRUE</b> (nonzero), the method enables AGC. If <b>FALSE</b>, it disables AGC.

### -param pguidEventContext [in]

Context value for the <a href="/windows/desktop/api/devicetopology/nf-devicetopology-icontrolchangenotify-onnotify">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetEnabled</b> call changes the state of the AGC control, all clients that have registered <a href="/windows/desktop/api/devicetopology/nn-devicetopology-icontrolchangenotify">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.

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

## -remarks

A disabled AGC control operates in pass-through mode. In this mode, the audio stream passes through the control without modification.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iaudioautogaincontrol">IAudioAutoGainControl Interface</a>