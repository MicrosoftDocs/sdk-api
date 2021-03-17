---
UID: NF:wcndevice.IWCNDevice.GetNetworkProfile
title: IWCNDevice::GetNetworkProfile (wcndevice.h)
description: The IWCNDevice::GetNetworkProfile method gets a network profile from the device.
helpviewer_keywords: ["GetNetworkProfile","GetNetworkProfile method [Windows Connect Now]","GetNetworkProfile method [Windows Connect Now]","IWCNDevice interface","IWCNDevice interface [Windows Connect Now]","GetNetworkProfile method","IWCNDevice.GetNetworkProfile","IWCNDevice::GetNetworkProfile","wcn.iwcndevice_getnetworkprofile","wcndevice/IWCNDevice::GetNetworkProfile"]
old-location: wcn\iwcndevice_getnetworkprofile.htm
tech.root: wcn
ms.assetid: a4fb0fc3-a45e-444c-953a-fe4fdfb0b327
ms.date: 12/05/2018
ms.keywords: GetNetworkProfile, GetNetworkProfile method [Windows Connect Now], GetNetworkProfile method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],GetNetworkProfile method, IWCNDevice.GetNetworkProfile, IWCNDevice::GetNetworkProfile, wcn.iwcndevice_getnetworkprofile, wcndevice/IWCNDevice::GetNetworkProfile
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
 - IWCNDevice::GetNetworkProfile
 - wcndevice/IWCNDevice::GetNetworkProfile
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
 - IWCNDevice.GetNetworkProfile
---

# IWCNDevice::GetNetworkProfile


## -description

The <b>IWCNDevice::GetNetworkProfile</b> method gets a network profile from the device.

## -parameters

### -param cchMaxStringLength [in]

The allocated size, in characters, of <i>wszProfile</i>.

### -param wszProfile [out]

 A string that specifies the XML WLAN network profile type.

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
The network profile was successfully retrieved.

</td>
</tr>
</table>

## -remarks

  This function can only be called after <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a> has been called, and the session has completed successfully.

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>



<a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-connect">IWCNDevice::Connect</a>