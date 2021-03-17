---
UID: NF:devicetopology.IConnector.IsConnected
title: IConnector::IsConnected (devicetopology.h)
description: The IsConnected method indicates whether this connector is connected to another connector.
helpviewer_keywords: ["IConnector interface [Core Audio]","IsConnected method","IConnector.IsConnected","IConnector::IsConnected","IConnectorIsConnected","IsConnected","IsConnected method [Core Audio]","IsConnected method [Core Audio]","IConnector interface","coreaudio.iconnector_isconnected","devicetopology/IConnector::IsConnected"]
old-location: coreaudio\iconnector_isconnected.htm
tech.root: CoreAudio
ms.assetid: 56aaee41-bf55-4556-b3d3-b0548a0db37c
ms.date: 12/05/2018
ms.keywords: IConnector interface [Core Audio],IsConnected method, IConnector.IsConnected, IConnector::IsConnected, IConnectorIsConnected, IsConnected, IsConnected method [Core Audio], IsConnected method [Core Audio],IConnector interface, coreaudio.iconnector_isconnected, devicetopology/IConnector::IsConnected
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
 - IConnector::IsConnected
 - devicetopology/IConnector::IsConnected
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
 - IConnector.IsConnected
---

# IConnector::IsConnected


## -description

The <b>IsConnected</b> method indicates whether this connector is connected to another connector.

## -parameters

### -param pbConnected [out]

Pointer to a <b>BOOL</b> variable into which the method writes the connection state. If the state is <b>TRUE</b>, this connector is connected to another connector. If <b>FALSE</b>, this connector is unconnected.

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
Pointer <i>pbConnected</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For a code example that calls the <b>IsConnected</b> method, see the implementation of the SelectCaptureDevice function in <a href="/windows/desktop/CoreAudio/device-topologies">Device Topologies</a>.

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>