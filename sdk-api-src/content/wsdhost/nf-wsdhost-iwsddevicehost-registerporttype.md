---
UID: NF:wsdhost.IWSDDeviceHost.RegisterPortType
title: IWSDDeviceHost::RegisterPortType (wsdhost.h)
description: Registers a port type for incoming messages.
helpviewer_keywords: ["IWSDDeviceHost interface","RegisterPortType method","IWSDDeviceHost.RegisterPortType","IWSDDeviceHost::RegisterPortType","RegisterPortType","RegisterPortType method","RegisterPortType method","IWSDDeviceHost interface","ncd.iwsddevicehost_registerporttype_method","wsdhost/IWSDDeviceHost::RegisterPortType"]
old-location: ncd\iwsddevicehost_registerporttype_method.htm
tech.root: ncd
ms.assetid: d514babb-c502-4d9a-b6c8-f371465cb9e8
ms.date: 12/05/2018
ms.keywords: IWSDDeviceHost interface,RegisterPortType method, IWSDDeviceHost.RegisterPortType, IWSDDeviceHost::RegisterPortType, RegisterPortType, RegisterPortType method, RegisterPortType method,IWSDDeviceHost interface, ncd.iwsddevicehost_registerporttype_method, wsdhost/IWSDDeviceHost::RegisterPortType
req.header: wsdhost.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdHost.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDDeviceHost::RegisterPortType
 - wsdhost/IWSDDeviceHost::RegisterPortType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDDeviceHost.RegisterPortType
---

# IWSDDeviceHost::RegisterPortType


## -description

Registers a port type for incoming messages.  All port types listed in the service host metadata must be registered.

## -parameters

### -param pPortType [in]

Reference to a <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_port_type">WSD_PORT_TYPE</a> structure that describes the port type.

## -returns

Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The port type specified by   <i>pPortType</i> has already been registered.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a>