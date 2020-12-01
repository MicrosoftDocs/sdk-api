---
UID: NF:wsdclient.IWSDDeviceProxy.Init
title: IWSDDeviceProxy::Init (wsdclient.h)
description: Initializes the device proxy, optionally sharing a session with a previously initialized sponsoring device proxy.
helpviewer_keywords: ["IWSDDeviceProxy interface","Init method","IWSDDeviceProxy.Init","IWSDDeviceProxy::Init","Init","Init method","Init method","IWSDDeviceProxy interface","ncd.iwsddeviceproxy_init_method","wsdclient/IWSDDeviceProxy::Init"]
old-location: ncd\iwsddeviceproxy_init_method.htm
tech.root: ncd
ms.assetid: d29212c8-2f29-41cc-ae35-8376ec5f0b7a
ms.date: 12/05/2018
ms.keywords: IWSDDeviceProxy interface,Init method, IWSDDeviceProxy.Init, IWSDDeviceProxy::Init, Init, Init method, Init method,IWSDDeviceProxy interface, ncd.iwsddeviceproxy_init_method, wsdclient/IWSDDeviceProxy::Init
req.header: wsdclient.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdClient.idl
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
 - IWSDDeviceProxy::Init
 - wsdclient/IWSDDeviceProxy::Init
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
 - IWSDDeviceProxy.Init
---

# IWSDDeviceProxy::Init


## -description

Initializes the device proxy, optionally sharing a session with a previously initialized sponsoring device proxy.

## -parameters

### -param pszDeviceId [in]

The logical address (ID) of the device.

### -param pDeviceAddress [in]

Reference to an <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a> object that contains the device configuration data.

### -param pszLocalId [in]

The logical address of the client. The logical address is of the form, urn:uuid:{guid}. Used when the server needs to initiate a connection to the client.

### -param pContext [in, optional]

Reference to an <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> object that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.

### -param pSponsor [in, optional]

Reference to an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object that is an optional device with which to share a session and lower layers.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszDeviceId</i> is <b>NULL</b>,  <i>pszLocalId</i> is <b>NULL</b>, or the length in characters of either identifier string exceeds WSD_MAX_TEXT_LENGTH (8192). 

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
</table>

## -remarks

This method is called by <a href="/windows/desktop/api/wsdclient/nf-wsdclient-wsdcreatedeviceproxy">WSDCreateDeviceProxy</a> and need not normally be called directly by the client code.

## -see-also

<a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a>