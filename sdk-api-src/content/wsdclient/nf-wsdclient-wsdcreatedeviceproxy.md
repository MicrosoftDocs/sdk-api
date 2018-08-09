---
UID: NF:wsdclient.WSDCreateDeviceProxy
title: WSDCreateDeviceProxy function
author: windows-sdk-content
description: Creates a device proxy and returns a pointer to the IWSDDeviceProxy interface.
old-location: ncd\wsdcreatedeviceproxy.htm
old-project: wsdapi
ms.assetid: d432ae9a-cf34-4149-978c-637443a3824f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSDCreateDeviceProxy, WSDCreateDeviceProxy function, ncd.wsdcreatedeviceproxy, wsdclient/WSDCreateDeviceProxy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateDeviceProxy
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDCreateDeviceProxy function


## -description


Creates a device proxy and returns a pointer to the  <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> interface.


## -parameters




### -param pszDeviceId [in]

The logical or physical address of the device. A logical address is of the form <code>urn:uuid:{guid}</code>. A physical address is a URI prefixed by http or https. If this address is a URI prefixed by https, then the proxy will use the SSL/TLS protocol.

The device address may be prefixed with the @ character. When <i>pszDeviceId</i> begins with @, this function does not retrieve the device metadata when creating the device proxy. 


### -param pszLocalId [in]

The logical or physical address of the client, which is used to identify the proxy and to act as an event sink endpoint. A logical address is of the form <code>urn:uuid:{guid}</code>. 

If the client uses a secure channel to receive events, then the address is a URI prefixed by https. This URI should specify port 5358, as this port is reserved for secure connections with WSDAPI. The port must be configured with an SSL server certificate before calling <a href="https://msdn.microsoft.com/31ddf62a-71d3-4f66-a704-2ee9e1fc8145">WSDCreateDeviceProxyAdvanced</a>. For more information about port configuration, see <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>.


### -param pContext [in]

An <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> object that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.


### -param ppDeviceProxy [out]

Pointer to an <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object that you use to represent a remote WSD device for client applications and middleware.


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
<i>pszDeviceId</i> is <b>NULL</b>, <i>pszLocalId</i> is <b>NULL</b>, the length in characters of <i>pszDeviceId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or the length in characters of  <i>pszLocalId</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

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



The <b>WSDCreateDeviceProxy</b> function calls the <a href="https://msdn.microsoft.com/d29212c8-2f29-41cc-ae35-8376ec5f0b7a">IWSDDeviceProxy::Init</a> method, which initializes an instance of an <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object.

This function will also retrieve the device metadata, unless the <i>pszDeviceId</i> parameter begins with the @ character. To retrieve device metadata after the device proxy has been created, call <a href="https://msdn.microsoft.com/8aa71ef1-61b9-411b-9e8c-75470c638469">IWSDDeviceProxy::BeginGetMetadata</a> and <a href="https://msdn.microsoft.com/c59ee37f-9189-4c32-8404-23cc94d76ad9">IWSDDeviceProxy::EndGetMetadata</a> on the returned <a href="https://msdn.microsoft.com/a1a54ba0-241a-4c3d-8113-89c0f8171c40">IWSDDeviceProxy</a> object.

For information about troubleshooting <b>WSDCreateDeviceProxy</b>function calls, see <a href="https://msdn.microsoft.com/befe4234-8d3a-4fc5-9a7d-faca94964af6">Troubleshooting WSDAPI Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/befe4234-8d3a-4fc5-9a7d-faca94964af6">Troubleshooting WSDAPI Applications</a>
 

 

