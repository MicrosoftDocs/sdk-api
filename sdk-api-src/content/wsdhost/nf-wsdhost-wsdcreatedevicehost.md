---
UID: NF:wsdhost.WSDCreateDeviceHost
title: WSDCreateDeviceHost function
author: windows-sdk-content
description: Creates a device host and returns a pointer to the IWSDDeviceHost interface.
old-location: ncd\wsdcreatedevicehost.htm
old-project: WsdApi
ms.assetid: dbe7ccd0-494d-4f6c-90f6-e729839d7008
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSDCreateDeviceHost, WSDCreateDeviceHost function, ncd.wsdcreatedevicehost, wsdhost/WSDCreateDeviceHost
ms.prod: windows
ms.technology: windows-sdk
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
 - WSDCreateDeviceHost
product: Windows
targetos: Windows
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDCreateDeviceHost function


## -description


Creates a device host and returns a pointer to the <a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a> interface.


## -parameters




### -param pszLocalId [in]

The logical or physical address of the device. A logical address is of the form <code>urn:uuid:{guid}</code>. If <i>pszLocalId</i> is a logical address, the host will announce the logical address and then convert the address to a physical address when it receives Resolve or Probe messages.


If <i>pszLocalId</i> is a physical address (such as  URL prefixed by http or https), the host will use the address as the physical address and will host on that address instead of the default one.


For secure communication, <i>pszLocalId</i> must be an URL prefixed by https, and the host will use the SSL/TLS protocol on the port specified in the URL.  The recommended port is port 5358, as this port is reserved for secure connections with WSDAPI.
If no port is specified, then the host will use port 443. The host port must be configured with an SSL server certificate before calling <b>WSDCreateDeviceHost</b>.  For more information about the configuration of host ports, see <a href="https://msdn.microsoft.com/b0a6d442-2ff4-4e00-8301-696fb0864d8c">HttpSetServiceConfiguration</a>.


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

An <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> object that defines custom message types or namespaces. 

If <b>NULL</b>, a default context representing the built-in message types and namespaces is used.


### -param ppDeviceHost [out]

Pointer to an <a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a> object that you use to expose the WSD-specific device semantics associated with a server that responds to incoming requests.


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



The <b>WSDCreateDeviceHost</b> function calls the <a href="https://msdn.microsoft.com/a66f0600-0bac-4bef-af43-6db60b60605e">IWSDDeviceHost::Init</a> method, which initializes an instance of an <a href="https://msdn.microsoft.com/497d0331-c88d-4381-8990-94227a9b9659">IWSDDeviceHost</a> object.






## -see-also




<a href="https://msdn.microsoft.com/8136fc01-9476-4ee4-aa44-784bef482ff5">WSDCreateDeviceHostAdvanced</a>
 

 

