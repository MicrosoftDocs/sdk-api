---
UID: NF:devicetopology.IAudioAutoGainControl.SetEnabled
title: IAudioAutoGainControl::SetEnabled
author: windows-sdk-content
description: The SetEnabled method enables or disables the AGC.
old-location: coreaudio\iaudioautogaincontrol_setenabled.htm
old-project: CoreAudio
ms.assetid: 05bf3b59-20e9-4bb0-931b-b6f28676cb5f
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: IAudioAutoGainControl interface [Core Audio],SetEnabled method, IAudioAutoGainControl.SetEnabled, IAudioAutoGainControl::SetEnabled, IAudioAutoGainControlSetEnabled, SetEnabled, SetEnabled method [Core Audio], SetEnabled method [Core Audio],IAudioAutoGainControl interface, coreaudio.iaudioautogaincontrol_setenabled, devicetopology/IAudioAutoGainControl::SetEnabled
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ConnectorType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IAudioAutoGainControl.SetEnabled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioAutoGainControl::SetEnabled


## -description



The <b>SetEnabled</b> method enables or disables the AGC.




## -parameters




### -param bEnable [in]

The new AGC state. If this parameter is <b>TRUE</b> (nonzero), the method enables AGC. If <b>FALSE</b>, it disables AGC.


### -param pguidEventContext [in]

Context value for the <a href="https://msdn.microsoft.com/a2f32cb9-3c8b-4b44-96a2-dd70afcca71a">IControlChangeNotify::OnNotify</a> method. This parameter points to an event-context GUID. If the <b>SetEnabled</b> call changes the state of the AGC control, all clients that have registered <a href="https://msdn.microsoft.com/e50e13c2-1ef3-46f6-8c53-f99cc1631a79">IControlChangeNotify</a> interfaces with that control receive notifications. In its implementation of the <b>OnNotify</b> method, a client can inspect the event-context GUID to discover whether it or another client is the source of the control-change event. If the caller supplies a <b>NULL</b> pointer for this parameter, the client's notification method receives a <b>NULL</b> context pointer.


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




<a href="https://msdn.microsoft.com/f21e27e6-f3a0-418a-ad2e-e3e104dd6da2">IAudioAutoGainControl Interface</a>
 

 

