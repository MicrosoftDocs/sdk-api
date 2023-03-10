---
UID: NF:wsdhost.WSDCreateDeviceHost
title: WSDCreateDeviceHost function (wsdhost.h)
description: Creates a device host and returns a pointer to the IWSDDeviceHost interface. (WSDCreateDeviceHost)
helpviewer_keywords: ["WSDCreateDeviceHost","WSDCreateDeviceHost function","ncd.wsdcreatedevicehost","wsdhost/WSDCreateDeviceHost"]
old-location: ncd\wsdcreatedevicehost.htm
tech.root: ncd
ms.assetid: dbe7ccd0-494d-4f6c-90f6-e729839d7008
ms.date: 12/05/2018
ms.keywords: WSDCreateDeviceHost, WSDCreateDeviceHost function, ncd.wsdcreatedevicehost, wsdhost/WSDCreateDeviceHost
req.header: wsdhost.h
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
 - WSDCreateDeviceHost
 - wsdhost/WSDCreateDeviceHost
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
 - WSDCreateDeviceHost
---

# WSDCreateDeviceHost function


## -description

Creates a device host and returns a pointer to the <a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a> interface.

## -parameters

### -param pszLocalId [in]

The logical or physical address of the device. A logical address is of the form <code>urn:uuid:{guid}</code>. If <i>pszLocalId</i> is a logical address, the host will announce the logical address and then convert the address to a physical address when it receives Resolve or Probe messages.


If <i>pszLocalId</i> is a physical address (such as  URL prefixed by http or https), the host will use the address as the physical address and will host on that address instead of the default one.


For secure communication, <i>pszLocalId</i> must be an URL prefixed by https, and the host will use the SSL/TLS protocol on the port specified in the URL.  The recommended port is port 5358, as this port is reserved for secure connections with WSDAPI.
If no port is specified, then the host will use port 443. The host port must be configured with an SSL server certificate before calling <b>WSDCreateDeviceHost</b>.  For more information about the configuration of host ports, see <a href="/windows/desktop/api/http/nf-http-httpsetserviceconfiguration">HttpSetServiceConfiguration</a>.


Any URL (http or https) must be terminated with a trailing slash. The URL must  contain a valid IP address or hostname.

The following list shows some example values for <i>pszLocalId</i>. It is not a complete list of valid values.

<ul>
<li>http://192.168.0.1:5357/</li>
<li>http://localhost/</li>
<li>http://myHostname:5357/
</li>
<li>https://192.168.0.1:5358/
</li>
<li>https://myHostname/
</li>
<li>https://myHostname/myDevice/
</li>
<li>https://myHostname:5358/
</li>
</ul>

### -param pContext [in]

An <a href="/windows/desktop/api/wsdxml/nn-wsdxml-iwsdxmlcontext">IWSDXMLContext</a> object that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.

### -param ppDeviceHost [out]

Pointer to an <a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a> object that you use to expose the WSD-specific device semantics associated with a server that responds to incoming requests.

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
<i>pszLocalId</i> is <b>NULL</b> or the length in characters of <i>pszLocalId</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppDeviceHost</i> is <b>NULL</b>.

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

The <b>WSDCreateDeviceHost</b> function calls the <a href="/windows/desktop/api/wsdhost/nf-wsdhost-iwsddevicehost-init">IWSDDeviceHost::Init</a> method, which initializes an instance of an <a href="/windows/desktop/api/wsdhost/nn-wsdhost-iwsddevicehost">IWSDDeviceHost</a> object.

## -see-also

<a href="/windows/desktop/api/wsdhost/nf-wsdhost-wsdcreatedevicehostadvanced">WSDCreateDeviceHostAdvanced</a>
