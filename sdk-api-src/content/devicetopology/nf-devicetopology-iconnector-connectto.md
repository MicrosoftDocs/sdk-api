---
UID: NF:devicetopology.IConnector.ConnectTo
title: IConnector::ConnectTo (devicetopology.h)
description: The ConnectTo method connects this connector to a connector in another device-topology object.
helpviewer_keywords: ["ConnectTo","ConnectTo method [Core Audio]","ConnectTo method [Core Audio]","IConnector interface","IConnector interface [Core Audio]","ConnectTo method","IConnector.ConnectTo","IConnector::ConnectTo","IConnectorConnectTo","coreaudio.iconnector_connectto","devicetopology/IConnector::ConnectTo"]
old-location: coreaudio\iconnector_connectto.htm
tech.root: CoreAudio
ms.assetid: 57704103-0124-4c02-8f96-980a50e98cca
ms.date: 12/05/2018
ms.keywords: ConnectTo, ConnectTo method [Core Audio], ConnectTo method [Core Audio],IConnector interface, IConnector interface [Core Audio],ConnectTo method, IConnector.ConnectTo, IConnector::ConnectTo, IConnectorConnectTo, coreaudio.iconnector_connectto, devicetopology/IConnector::ConnectTo
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
 - IConnector::ConnectTo
 - devicetopology/IConnector::ConnectTo
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
 - IConnector.ConnectTo
---

# IConnector::ConnectTo


## -description

The <b>ConnectTo</b> method connects this connector to a connector in another device-topology object.

## -parameters

### -param pConnectTo [in]

The other connector. This parameter points to the <a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector</a> interface of the connector object that represents the connector in the other device topology. The caller is responsible for releasing its counted reference to the <b>IConnector</b> interface when it is no longer needed. The <b>ConnectTo</b> method obtains its own reference to this interface.

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
Pointer <i>pConnectTo</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The current connector and remote connector pointed to by <i>pConnectTo</i>, have the same direction of data flow. A connector with data-flow direction "In" must be connected to another connector with data-flow direction "Out" to create a valid connection in the topology. To determine the data flow of a connector, call <a href="/windows/desktop/api/devicetopology/nf-devicetopology-iconnector-getdataflow">IConnector::GetDataFlow</a>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object pointed to by <i>pConnectTo</i> is not a valid connector object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_DEVICE_ALREADY_ATTACHED)</b></dt>
</dl>
</td>
<td width="60%">
One of the two connectors is already attached to another connector. For information about this macro, see the Windows SDK documentation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iconnector">IConnector Interface</a>