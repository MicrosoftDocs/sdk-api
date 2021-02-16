---
UID: NF:certadm.IOCSPAdmin.SetConfiguration
title: IOCSPAdmin::SetConfiguration (certadm.h)
description: Updates a responder service with configuration changes.
helpviewer_keywords: ["IOCSPAdmin interface [Security]","SetConfiguration method","IOCSPAdmin.SetConfiguration","IOCSPAdmin::SetConfiguration","SetConfiguration","SetConfiguration method [Security]","SetConfiguration method [Security]","IOCSPAdmin interface","certadm/IOCSPAdmin::SetConfiguration","security.iocspadmin_setconfiguration_method"]
old-location: security\iocspadmin_setconfiguration_method.htm
tech.root: security
ms.assetid: 973c69c3-282b-4e17-bb44-119965a4b443
ms.date: 12/05/2018
ms.keywords: IOCSPAdmin interface [Security],SetConfiguration method, IOCSPAdmin.SetConfiguration, IOCSPAdmin::SetConfiguration, SetConfiguration, SetConfiguration method [Security], SetConfiguration method [Security],IOCSPAdmin interface, certadm/IOCSPAdmin::SetConfiguration, security.iocspadmin_setconfiguration_method
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
 - IOCSPAdmin::SetConfiguration
 - certadm/IOCSPAdmin::SetConfiguration
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
 - IOCSPAdmin.SetConfiguration
---

# IOCSPAdmin::SetConfiguration


## -description

The <b>SetConfiguration</b> method updates a responder service  with configuration changes.

## -parameters

### -param bstrServerName [in]

A string that contains the responder-service name.

### -param bForce [in]

<table>
<tr>
<td><strong>C++</strong></td>
<td><b>VARIANT_TRUE</b> if the method should update the responder service registry when the service is offline or unavailable; otherwise, <b>VARIANT_FALSE</b>. If the service is offline or unavailable and the <i>bForce</i> parameter is <b>VARIANT_TRUE</b>, <b>SetConfiguration</b> updates the responder service registry directly.

</td>
</tr>
<tr>
<td><strong>VB</strong></td>
<td><b>True</b> if the method should update the responder service registry when the service is offline or unavailable; otherwise, <b>False</b>. If the service is offline or unavailable and the <i>bForce</i> parameter is <b>True</b>, <b>SetConfiguration</b> updates the responder service registry directly.

</td>
</tr>
</table>

## -returns

<h3>VB</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>