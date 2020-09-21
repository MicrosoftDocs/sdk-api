---
UID: NF:devicetopology.IConnector.GetConnectedTo
title: IConnector::GetConnectedTo (devicetopology.h)
description: The GetConnectedTo method gets the connector to which this connector is connected.
helpviewer_keywords: ["GetConnectedTo","GetConnectedTo method [Core Audio]","GetConnectedTo method [Core Audio]","IConnector interface","IConnector interface [Core Audio]","GetConnectedTo method","IConnector.GetConnectedTo","IConnector::GetConnectedTo","IConnectorGetConnectedTo","coreaudio.iconnector_getconnectedto","devicetopology/IConnector::GetConnectedTo"]
old-location: coreaudio\iconnector_getconnectedto.htm
tech.root: CoreAudio
ms.assetid: bee0187c-5650-4b54-89b7-e63874048ed0
ms.date: 12/05/2018
ms.keywords: GetConnectedTo, GetConnectedTo method [Core Audio], GetConnectedTo method [Core Audio],IConnector interface, IConnector interface [Core Audio],GetConnectedTo method, IConnector.GetConnectedTo, IConnector::GetConnectedTo, IConnectorGetConnectedTo, coreaudio.iconnector_getconnectedto, devicetopology/IConnector::GetConnectedTo
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
 - IConnector::GetConnectedTo
 - devicetopology/IConnector::GetConnectedTo
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
 - IConnector.GetConnectedTo
---

# IConnector::GetConnectedTo


## -description

The <b>GetConnectedTo</b> method gets the connector to which this connector is connected.

## -parameters

### -param ppConTo [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> interface of the other connector object. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetConnectedTo</b> call fails,  <i>*ppConTo</i> is <b>NULL</b>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppConTo</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
This connector is not connected, or the other side of the connection is not another device topology (for example, a Software_IO connection).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_PATH_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The device topology on the other side of the connection is not active (that is, the device state is not DEVICE_STATE_ACTIVE).

</td>
</tr>
</table>

## -remarks

For code examples that call this method, see the implementations of the GetHardwareDeviceTopology and SelectCaptureDevice functions in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

For information about Software_IO connections, see <a href="/windows/win32/api/devicetopology/ne-devicetopology-connectortype">ConnectorType Enumeration</a>. For information about the HRESULT_FROM_WIN32 macro, see the Windows SDK documentation. For information about the DEVICE_STATE_NOTPRESENT device state, see <a href="/windows/desktop/CoreAudio/device-state-xxx-constants">DEVICE_STATE_XXX Constants</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>