---
UID: NF:wsdclient.WSDCreateDeviceProxyAdvanced
title: WSDCreateDeviceProxyAdvanced function (wsdclient.h)
description: Creates a device proxy and returns a pointer to the IWSDDeviceProxy interface. (WSDCreateDeviceProxyAdvanced)
helpviewer_keywords: ["WSDCreateDeviceProxyAdvanced","WSDCreateDeviceProxyAdvanced function","ncd.wsdcreatedeviceproxyadvanced","wsdclient/WSDCreateDeviceProxyAdvanced"]
old-location: ncd\wsdcreatedeviceproxyadvanced.htm
tech.root: ncd
ms.assetid: 31ddf62a-71d3-4f66-a704-2ee9e1fc8145
ms.date: 12/05/2018
ms.keywords: WSDCreateDeviceProxyAdvanced, WSDCreateDeviceProxyAdvanced function, ncd.wsdcreatedeviceproxyadvanced, wsdclient/WSDCreateDeviceProxyAdvanced
req.header: wsdclient.h
req.include-header: Wsdapi.h
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
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSDCreateDeviceProxyAdvanced
 - wsdclient/WSDCreateDeviceProxyAdvanced
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateDeviceProxyAdvanced
---

# WSDCreateDeviceProxyAdvanced function


## -description

Creates a device proxy and returns a pointer to the  <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> interface.

## -parameters

### -param pszDeviceId [in]

The logical or physical address of the device. A logical address is of the form <code>urn:uuid:{guid}</code>. A physical address is a URI prefixed by http or https. If this address is a URI prefixed by https, then the proxy will use the SSL/TLS protocol. 

If either <i>pszDeviceId</i> or the <i>pszLocalId</i> is an URL prefixed by https, then both URLs must be identical. If this is not the case, <b>WSDCreateDeviceProxyAdvanced</b> will return E_INVALIDARG. 

The device address may be prefixed with the @ character. When <i>pszDeviceId</i> begins with @, this function does not retrieve the device metadata when creating the device proxy.

### -param pDeviceAddress

An <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a> interface that defines the device transport address. When <i>pDeviceAddress</i> is specified, a device proxy can be created without requiring the resolution of a logical address passed to <i>pszDeviceId</i>. This parameter may be <b>NULL</b>.

### -param pszLocalId [in]

The logical or physical address of the client, which is used to identify the proxy and to act as an event sink endpoint. A logical address is of the form <code>urn:uuid:{guid}</code>. 

If the client uses a secure channel to receive events, then the address is a URI prefixed by https. This URI should specify port 5358, as this port is reserved for secure connections with WSDAPI. The port must be configured with an SSL server certificate before calling <b>WSDCreateDeviceProxyAdvanced</b>. For more information about port configuration, see <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>.

### -param pContext [in]

An <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> interface that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.

### -param ppDeviceProxy [out]

Pointer to the <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> interface that you use to represent a remote WSD device for client applications and middleware.

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
<i>pszDeviceId</i> is <b>NULL</b>, <i>pszLocalId</i> is <b>NULL</b>, the length in characters of <i>pszDeviceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), the length in characters of <i>pszLocalId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or <i>pszDeviceId</i> points to a URI prefixed by https and that URL does not match the URI passed to <i>pszLocalId</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppDeviceProxy</i> is <b>NULL</b>.

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

The <b>WSDCreateDeviceProxyAdvanced</b> function calls the <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-init">IWSDDeviceProxy::Init</a> method, which initializes an instance of an <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object.



This function will also retrieve the device metadata, unless the <i>pszDeviceId</i> parameter begins with the @ character. To retrieve device metadata after the device proxy has been created, call <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-begingetmetadata">IWSDDeviceProxy::BeginGetMetadata</a> and <a href="/windows/desktop/api/wsdclient/nf-wsdclient-iwsddeviceproxy-endgetmetadata">IWSDDeviceProxy::EndGetMetadata</a> on the returned <a href="/windows/desktop/api/wsdclient/nn-wsdclient-iwsddeviceproxy">IWSDDeviceProxy</a> object.

For information about troubleshooting <b>WSDCreateDeviceProxyAdvanced</b> function calls, see <a href="/windows/desktop/WsdApi/troubleshooting-wsdapi-applications">Troubleshooting WSDAPI Applications</a>.

## -see-also

<a href="/windows/desktop/WsdApi/troubleshooting-wsdapi-applications">Troubleshooting WSDAPI Applications</a>
