---
UID: NF:mbnapi.IMbnConnection.GetVoiceCallState
title: IMbnConnection::GetVoiceCallState (mbnapi.h)
description: Gets the voice call state of the device.
helpviewer_keywords: ["GetVoiceCallState","GetVoiceCallState method [Microsoft Broadband Networks]","GetVoiceCallState method [Microsoft Broadband Networks]","IMbnConnection interface","IMbnConnection interface [Microsoft Broadband Networks]","GetVoiceCallState method","IMbnConnection.GetVoiceCallState","IMbnConnection::GetVoiceCallState","mbn.imbnconnection_getvoicecallstate","mbnapi/IMbnConnection::GetVoiceCallState"]
old-location: mbn\imbnconnection_getvoicecallstate.htm
tech.root: mbn
ms.assetid: a715f7c8-a001-41a2-9c1f-ca133568133b
ms.date: 12/05/2018
ms.keywords: GetVoiceCallState, GetVoiceCallState method [Microsoft Broadband Networks], GetVoiceCallState method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],GetVoiceCallState method, IMbnConnection.GetVoiceCallState, IMbnConnection::GetVoiceCallState, mbn.imbnconnection_getvoicecallstate, mbnapi/IMbnConnection::GetVoiceCallState
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - IMbnConnection::GetVoiceCallState
 - mbnapi/IMbnConnection::GetVoiceCallState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnection.GetVoiceCallState
---

# IMbnConnection::GetVoiceCallState


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the voice call state of the device.

## -parameters

### -param voiceCallState [out, retval]

A pointer to a <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_voice_call_state">MBN_VOICE_CALL_STATE</a> value that specifies the voice call state.  If the method returns anything other than <b>S_OK</b>, the contents of this pointer are not set.

## -returns

This method can return one of these values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The call state not available.  The Mobile Broadband service is probing the device for the information.  The calling application can be notified when the call state is available by registering for the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionevents-onvoicecallstatechange">OnVoiceCallStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required to get the call state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
A SIM is not inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
</table>

## -remarks

For the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>,  the Mobile Broadband service will query the device again for this information once the error condition is over. For example, if the device required a PIN to be entered to retrieve the voice call state, then <b>E_MBN_PIN_REQUIRED</b> is returned. After the calling application enters the PIN to unlock the device, the Mobile Broadband service will again try to get the voice call state from the device. The Mobile Broadband service will update the application with the status of a new probe by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionevents-onvoicecallstatechange">OnVoiceCallStateChange</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a>