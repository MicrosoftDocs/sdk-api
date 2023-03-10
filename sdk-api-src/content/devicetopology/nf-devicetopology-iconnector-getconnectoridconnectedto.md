---
UID: NF:devicetopology.IConnector.GetConnectorIdConnectedTo
title: IConnector::GetConnectorIdConnectedTo (devicetopology.h)
description: The GetConnectorIdConnectedTo method gets the global ID of the connector, if any, that this connector is connected to.
helpviewer_keywords: ["GetConnectorIdConnectedTo","GetConnectorIdConnectedTo method [Core Audio]","GetConnectorIdConnectedTo method [Core Audio]","IConnector interface","IConnector interface [Core Audio]","GetConnectorIdConnectedTo method","IConnector.GetConnectorIdConnectedTo","IConnector::GetConnectorIdConnectedTo","IConnectorGetConnectorIdConnectedTo","coreaudio.iconnector_getconnectoridconnectedto","devicetopology/IConnector::GetConnectorIdConnectedTo"]
old-location: coreaudio\iconnector_getconnectoridconnectedto.htm
tech.root: CoreAudio
ms.assetid: 865add93-9174-41c5-8998-b68f75eb35a1
ms.date: 12/05/2018
ms.keywords: GetConnectorIdConnectedTo, GetConnectorIdConnectedTo method [Core Audio], GetConnectorIdConnectedTo method [Core Audio],IConnector interface, IConnector interface [Core Audio],GetConnectorIdConnectedTo method, IConnector.GetConnectorIdConnectedTo, IConnector::GetConnectorIdConnectedTo, IConnectorGetConnectorIdConnectedTo, coreaudio.iconnector_getconnectoridconnectedto, devicetopology/IConnector::GetConnectorIdConnectedTo
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
 - IConnector::GetConnectorIdConnectedTo
 - devicetopology/IConnector::GetConnectorIdConnectedTo
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
 - IConnector.GetConnectorIdConnectedTo
---

# IConnector::GetConnectorIdConnectedTo


## -description

The <b>GetConnectorIdConnectedTo</b> method gets the global ID of the connector, if any, that this connector is connected to.

## -parameters

### -param ppwstrConnectorId [out]

Pointer to a string pointer into which the method writes the address of a null-terminated, wide-character string that contains the other connector's global ID. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetConnectorIdConnectedTo</b> call fails,  <i>*ppwstrConnectorId</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppwstrConnectorId</i> is <b>NULL</b>.

</td>
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

A global ID is a string that uniquely identifies a part among all parts in all device topologies in the system. Clients should treat this string as opaque. That is, clients should not attempt to parse the contents of the string to obtain information about the part. The reason is that the string format is undefined and might change from one implementation of the DeviceTopology API to the next.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>