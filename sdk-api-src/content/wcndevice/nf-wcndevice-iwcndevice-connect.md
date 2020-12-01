---
UID: NF:wcndevice.IWCNDevice.Connect
title: IWCNDevice::Connect (wcndevice.h)
description: The IWCNDevice::Connect method initiates the session.
helpviewer_keywords: ["Connect","Connect method [Windows Connect Now]","Connect method [Windows Connect Now]","IWCNDevice interface","IWCNDevice interface [Windows Connect Now]","Connect method","IWCNDevice.Connect","IWCNDevice::Connect","wcn.iwcndevice_connect","wcndevice/IWCNDevice::Connect"]
old-location: wcn\iwcndevice_connect.htm
tech.root: wcn
ms.assetid: d7c940f2-0862-4b53-bbb9-4ea47fe6d6f6
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [Windows Connect Now], Connect method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],Connect method, IWCNDevice.Connect, IWCNDevice::Connect, wcn.iwcndevice_connect, wcndevice/IWCNDevice::Connect
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
 - IWCNDevice::Connect
 - wcndevice/IWCNDevice::Connect
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
 - IWCNDevice.Connect
---

# IWCNDevice::Connect


## -description

The <b>IWCNDevice::Connect</b> method initiates the session.

## -parameters

### -param pNotify [in]

A pointer to the implemented <a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a> callback interface which specifies if a connection has been successfully established.

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
The operation has succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The device does not support the connection options queued via IWCNDevice::Set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WCN_E_PEER_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The device could not be located on the network.

</td>
</tr>
</table>

## -remarks

After calling this method you may not call any other <a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a> 'Set' methods.  There is no way to cancel or roll back device settings once a connection has been established.

<b>NULL</b>  can be passed via pNotify, in place of  the <a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a> callback interface to prevent  notification from being sent when the connect operation is complete.

## -see-also

<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcnconnectnotify">IWCNConnectNotify</a>



<a href="/windows/desktop/api/wcndevice/nn-wcndevice-iwcndevice">IWCNDevice</a>