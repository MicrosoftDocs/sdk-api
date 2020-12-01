---
UID: NF:mbnapi.IMbnRadio.SetSoftwareRadioState
title: IMbnRadio::SetSoftwareRadioState (mbnapi.h)
description: Sets the software radio state of a Mobile Broadband device.
helpviewer_keywords: ["IMbnRadio interface [Microsoft Broadband Networks]","SetSoftwareRadioState method","IMbnRadio.SetSoftwareRadioState","IMbnRadio::SetSoftwareRadioState","SetSoftwareRadioState","SetSoftwareRadioState method [Microsoft Broadband Networks]","SetSoftwareRadioState method [Microsoft Broadband Networks]","IMbnRadio interface","mbn.imbnradio_setsoftwareradiostate","mbnapi/IMbnRadio::SetSoftwareRadioState"]
old-location: mbn\imbnradio_setsoftwareradiostate.htm
tech.root: mbn
ms.assetid: d140109d-5659-42aa-b645-996dfc5a9d4e
ms.date: 12/05/2018
ms.keywords: IMbnRadio interface [Microsoft Broadband Networks],SetSoftwareRadioState method, IMbnRadio.SetSoftwareRadioState, IMbnRadio::SetSoftwareRadioState, SetSoftwareRadioState, SetSoftwareRadioState method [Microsoft Broadband Networks], SetSoftwareRadioState method [Microsoft Broadband Networks],IMbnRadio interface, mbn.imbnradio_setsoftwareradiostate, mbnapi/IMbnRadio::SetSoftwareRadioState
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnRadio::SetSoftwareRadioState
 - mbnapi/IMbnRadio::SetSoftwareRadioState
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
 - IMbnRadio.SetSoftwareRadioState
---

# IMbnRadio::SetSoftwareRadioState


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Sets the software radio state of  a Mobile Broadband device.

## -parameters

### -param radioState [in]

A <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_radio">MBN_RADIO</a> value that specifies the new software radio state.

### -param requestID [out]

A pointer to a request ID assigned by the Mobile Broadband service to identify this request.

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
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid.  Most likely,the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid. Most likely the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_SERVICE_NOT_ACTIVE)</b></dt>
</dl>
</td>
<td width="60%">
The Mobile Broadband service is not running on this system.

</td>
</tr>
</table>

## -remarks

<b>SetSoftwareRadioState</b> changes the software radio state of the device. This is an asynchronous operation and it will return immediately. On completion, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnradioevents-onsetsoftwareradiostatecomplete">OnSetSoftwareRadioStateComplete</a> method of the  <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnradioevents">IMbnRadioEvents</a> interface. 


Disabling the radio for a Mobile Broadband device will result in deactivation of any active connection, network packet detach, and network deregistration. If the radio off operation results in a change in the connection state, packet attach state, or network registration state, then the application will receive a notification of the changes.


When both software and hardware radio are enabled for a Mobile Broadband device, it will automatically try to register to the network.  Also, some devices may also try to a perform packet attach to the network. Whenever the state changes, the calling application will receive event notifications for network registration and packet attach state changes.



A device's radio state can change without a change request from the application.  For instance, if a user turns on the system's hardware radio switch.  The Mobile Broadband service will notify the application about a change in radio state by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnradioevents-onradiostatechange">OnRadioStateChange</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnradioevents">IMbnRadioEvents</a> interface.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnradio">IMbnRadio</a>