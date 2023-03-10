---
UID: NF:wcndevice.IWCNDevice.SetNetworkProfile
title: IWCNDevice::SetNetworkProfile (wcndevice.h)
description: The IWCNDevice::SetNetworkProfile method queues an XML WLAN profile to be provisioned to the device. This method may only be called prior to IWCNDevice::Connect.
helpviewer_keywords: ["IWCNDevice interface [Windows Connect Now]","SetNetworkProfile method","IWCNDevice.SetNetworkProfile","IWCNDevice::SetNetworkProfile","SetNetworkProfile","SetNetworkProfile method [Windows Connect Now]","SetNetworkProfile method [Windows Connect Now]","IWCNDevice interface","wcn.iwcndevice_setnetworkprofile","wcndevice/IWCNDevice::SetNetworkProfile"]
old-location: wcn\iwcndevice_setnetworkprofile.htm
tech.root: wcn
ms.assetid: 267aa55a-005d-4db8-9569-f8ee77a15168
ms.date: 12/05/2018
ms.keywords: IWCNDevice interface [Windows Connect Now],SetNetworkProfile method, IWCNDevice.SetNetworkProfile, IWCNDevice::SetNetworkProfile, SetNetworkProfile, SetNetworkProfile method [Windows Connect Now], SetNetworkProfile method [Windows Connect Now],IWCNDevice interface, wcn.iwcndevice_setnetworkprofile, wcndevice/IWCNDevice::SetNetworkProfile
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
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
 - IWCNDevice::SetNetworkProfile
 - wcndevice/IWCNDevice::SetNetworkProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNDevice.SetNetworkProfile
---

# IWCNDevice::SetNetworkProfile


## -description

The <b>IWCNDevice::SetNetworkProfile</b> method queues an XML WLAN profile to be provisioned to the device.  This method may  only be called prior to <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>.

## -parameters

### -param pszProfileXml [in]

The XML WLAN profile XML string.

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
The attribute was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The WLAN profile is not supported for WCN connections.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_BAD_PROFILE)</b></dt>
</dl>
</td>
<td width="60%">
The provided XML profile cannot be read.

</td>
</tr>
</table>

## -remarks

Currently, the <b>Windows Connect Now API</b> (WCNAPI) supports the following profile types: <ul>
<li>None (Open or Shared)</li>
<li>WEP (Open or Shared)</li>
<li>WPA-PSK (TKIP or AES)</li>
<li>WPA2-PSK (TKIP or AES)</li>
</ul>   If  the specified WLAN profile has extraneous settings (like IHV settings), these settings will be ignored. In the event a WLAN profile is not  compatible with the WCNAPI, an <b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b> value is returned.

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>