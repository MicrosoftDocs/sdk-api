---
UID: NF:devicetopology.IAudioMute.SetMute
title: IAudioMute::SetMute
author: windows-sdk-content
description: The SetMute method enables or disables the mute control.
old-location: coreaudio\iaudiomute_setmute.htm
tech.root: CoreAudio
ms.assetid: e99cb894-b39e-42ec-be8f-dc3fa6e7abcd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAudioMute interface [Core Audio],SetMute method, IAudioMute.SetMute, IAudioMute::SetMute, IAudioMuteSetMute, SetMute, SetMute method [Core Audio], SetMute method [Core Audio],IAudioMute interface, coreaudio.iaudiomute_setmute, devicetopology/IAudioMute::SetMute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioMute.SetMute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- devicetopology.h
: 
- IAudioMute.SetMute
: 
---

# IAudioMute::SetMute


## -description



The <b>SetMute</b> method enables or disables the mute control.




## -parameters




### -param bMuted [in]

The new muting state. If <i>bMuted</i> is <b>TRUE</b> (nonzero), the method enables muting. If <b>FALSE</b>, the method disables muting.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a2f32cb9-3c8b-4b44-96a2-dd70afcca71a">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetMute</b> call changes the state of the mute control, all clients that have registered <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


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




<a href="https://msdn.microsoft.com/53d49af7-81c3-4e75-ba06-dcee34d84292">IAudioMute Interface</a>
 

 

