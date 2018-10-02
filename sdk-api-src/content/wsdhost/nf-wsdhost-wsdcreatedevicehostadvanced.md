---
UID: NF:wsdhost.WSDCreateDeviceHostAdvanced
title: WSDCreateDeviceHostAdvanced function
author: windows-sdk-content
description: Creates a device host and returns a pointer to the IWSDDeviceHost interface.
old-location: ncd\wsdcreatedevicehostadvanced.htm
tech.root: WsdApi
ms.assetid: 8136fc01-9476-4ee4-aa44-784bef482ff5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSDCreateDeviceHostAdvanced, WSDCreateDeviceHostAdvanced function, ncd.wsdcreatedevicehostadvanced, wsdhost/WSDCreateDeviceHostAdvanced
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateDeviceHostAdvanced
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSDCreateDeviceHostAdvanced function


## -description


Creates a device host and returns  a pointer to the <a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a> interface.


## -parameters




### -param pszLocalId [in]

The logical or physical address of the device. A logical address is of the form <code>urn:uuid:{guid}</code>. If <i>pszLocalId</i> is a logical address, the host will announce the logical address and then convert the address to a physical address when it receives Resolve or Probe messages.

If <i>pszLocalId</i> is a physical address (such as  URL prefixed by http or https), the host will use the address as the physical address and will host on that address instead of the default one.


For secure communication, <i>pszLocalId</i> must be an URL prefixed by https, and the host will use the SSL/TLS protocol on the port specified in the URL.  The recommended port is port 5358, as this port is reserved for secure connections with WSDAPI.
If no port is specified, then the host will use port 443. The host port must be configured with an SSL server certificate before calling <b>WSDCreateDeviceHostAdvanced</b>.  For more information about the configuration of host ports, see <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>.


If either <i>pszLocalId</i> or the transport address referenced by <i>ppHostAddresses</i> is an URL prefixed by https, then both URLs must be identical. If this is not the case, <b>WSDCreateDeviceHostAdvanced</b> will return E_INVALIDARG. 

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

An <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> interface that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.


### -param ppHostAddresses [in]

A single <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> interface or <a href="https://msdn.microsoft.com/84dfee11-8092-4018-8840-e766a94c60a4">IWSDTransportAddress</a> interface. The objects provide information about specific addresses that the host should listen on.

If <i>pszLocalId</i> contains a logical address, the resulting behavior is a mapping between the logical address and a specific set of physical addresses (instead of a mapping between the logical address and a default physical address).


### -param dwHostAddressCount [in]

The number of items in the <i>ppHostAddresses</i> array. If <i>ppHostAddresses</i> is an <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> interface, count must be 1.


### -param ppDeviceHost [out]

Pointer to the <a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a> interface that you use to expose the WSD-specific device semantics associated with a server that responds to incoming requests.


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
<i>pszLocalId</i> is <b>NULL</b>, the length in characters of <i>pszLocalId</i> exceeds WSD_MAX_TEXT_LENGTH (8192), or <i>pszLocalId</i> points to an URL prefixed by https and that URL does not match the URL of the transport address referenced by <i>ppHostAddresses</i>.

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



The <b>WSDCreateDeviceHostAdvanced</b> function calls the <a href="https://msdn.microsoft.com/a66f0600-0bac-4bef-af43-6db60b60605e">IWSDDeviceHost::Init</a> method, which initializes an instance of an <a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a> object.






## -see-also




<a href="https://msdn.microsoft.com/dbe7ccd0-494d-4f6c-90f6-e729839d7008">WSDCreateDeviceHost</a>
 

 

