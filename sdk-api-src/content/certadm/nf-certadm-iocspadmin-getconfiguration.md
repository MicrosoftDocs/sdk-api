---
UID: NF:certadm.IOCSPAdmin.GetConfiguration
title: IOCSPAdmin::GetConfiguration (certadm.h)
description: Connects to an Online Certificate Status Protocol (OCSP) responder server and initializes an OCSPAdmin object with the configuration information from the server.
helpviewer_keywords: ["GetConfiguration","GetConfiguration method [Security]","GetConfiguration method [Security]","IOCSPAdmin interface","IOCSPAdmin interface [Security]","GetConfiguration method","IOCSPAdmin.GetConfiguration","IOCSPAdmin::GetConfiguration","certadm/IOCSPAdmin::GetConfiguration","security.iocspadmin_getconfiguration_method"]
old-location: security\iocspadmin_getconfiguration_method.htm
tech.root: security
ms.assetid: bf3c5757-0e97-46d2-89c2-f62a5e367fbb
ms.date: 12/05/2018
ms.keywords: GetConfiguration, GetConfiguration method [Security], GetConfiguration method [Security],IOCSPAdmin interface, IOCSPAdmin interface [Security],GetConfiguration method, IOCSPAdmin.GetConfiguration, IOCSPAdmin::GetConfiguration, certadm/IOCSPAdmin::GetConfiguration, security.iocspadmin_getconfiguration_method
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPAdmin::GetConfiguration
 - certadm/IOCSPAdmin::GetConfiguration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPAdmin.GetConfiguration
---

# IOCSPAdmin::GetConfiguration


## -description

The <b>GetConfiguration</b> method connects to an Online Certificate Status Protocol (OCSP) responder server and initializes an <b>OCSPAdmin</b> object with the configuration information from the server.

## -parameters

### -param bstrServerName [in]

A string that contains the responder-server name.

### -param bForce [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td>
<b>VARIANT_TRUE</b> if the caller wants to read the responder configuration from the server's registry when a running instance of the OCSP responder service cannot be found; otherwise, <b>VARIANT_FALSE</b>.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td>
<b>True</b> if the caller wants to read the responder configuration from the server's registry when a running instance of the OCSP responder service cannot be found; otherwise, <b>False</b>.

</td>
</tr>
</table>

## -returns

<h3>VB</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

If the method returns <b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b>, the configuration is already initialized.

If the method returns <b>E_INVALIDARG</b>, the <i>pVal</i> parameter was set to <b>NULL</b>.

## -remarks

The following table lists the effects of the <i>bForce</i> parameter value on the method call.

<table>
<tr>
<th>OCSP responder service on the target server</th>
<th><i>bForce</i> is <b>VARIANT_TRUE</b></th>
<th><i>bForce</i> is <b>VARIANT_FALSE</b></th>
</tr>
<tr>
<td>
Running

</td>
<td>
Retrieve configuration from the service.

</td>
<td>
Retrieve configuration from the service.

</td>
</tr>
<tr>
<td>
Stopped

</td>
<td>
Attempt to retrieve configuration from the server registry. If this attempt fails, return an error.

</td>
<td>
Return an error.

</td>
</tr>
</table>
 

The following table lists the effects of the <i>bForce</i> parameter value on the method call.

<table>
<tr>
<th>OCSP responder service on the target server</th>
<th><i>bForce</i> is <b>True</b></th>
<th><i>bForce</i> is <b>False</b></th>
</tr>
<tr>
<td>
Running

</td>
<td>
Retrieve configuration from the service.

</td>
<td>
Retrieve configuration from the service.

</td>
</tr>
<tr>
<td>
Stopped

</td>
<td>
Attempt to retrieve configuration from the server registry. If this attempt fails, return an error.

</td>
<td>
Return an error.

</td>
</tr>
</table>
 

This method attempts to read the configuration from a running instance of an OCSP responder service, but that might not be possible if the service is not running or is in an inaccessible state. The caller can instruct the method to read the configuration from the server's registry if a running instance cannot be found.

The method fails if you try to call it more than once for a given <b>OCSPAdmin</b> object. Each instance of <b>OCSPAdmin</b> corresponds to one responder server. To connect to another server in an array of OCSP responder servers, create a new instance of an <b>OCSPAdmin</b> object.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>