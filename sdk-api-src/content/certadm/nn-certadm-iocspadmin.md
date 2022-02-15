---
UID: NN:certadm.IOCSPAdmin
title: IOCSPAdmin (certadm.h)
description: Provides functionality to manage an Online Certificate Status Protocol (OCSP) responder server.
helpviewer_keywords: ["IOCSPAdmin","IOCSPAdmin interface [Security]","IOCSPAdmin interface [Security]","described","OCSPAdmin object","certadm/IOCSPAdmin","security.iocspadmin"]
old-location: security\iocspadmin.htm
tech.root: security
ms.assetid: cf76e934-07a2-46de-b2cf-7f6d3e274d71
ms.date: 12/05/2018
ms.keywords: IOCSPAdmin, IOCSPAdmin interface [Security], IOCSPAdmin interface [Security],described, OCSPAdmin object, certadm/IOCSPAdmin, security.iocspadmin
req.header: certadm.h
req.include-header: 
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
 - IOCSPAdmin
 - certadm/IOCSPAdmin
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
 - IOCSPAdmin
---

# IOCSPAdmin interface


## -description

The <b>IOCSPAdmin</b> interface provides functionality to manage an Online Certificate Status Protocol (OCSP) responder server. Implement this interface to manage individual responder server properties and <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) definitions. After creating an instance of this interface, you call <a href="/windows/desktop/api/certadm/nf-certadm-iocspadmin-getconfiguration">GetConfiguration</a> to connect to a responder service and initialize an <b>OCSPAdmin</b> object. Each <b>OCSPAdmin</b> object corresponds to one physical responder server.
<div class="alert"><b>Note</b>  This interface does not include functionality to  create or parse certificate status requests.</div><div> </div>In C++, you create an instance of this interface by calling the <b>CoCreateInstance</b> function with the <b>CLSID_OCSPAdmin</b> class identifier.

In Visual Basic Scripting Edition, you create an instance of the <b>OCSPAdmin</b> object.

## -inheritance

The <b>IOCSPAdmin</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IOCSPAdmin</b> also has these types of members:

## -remarks

The following table disambiguates the various properties used in the Microsoft OCSP architecture.

<table>
<tr>
<th>Architecture</th>
<th>Scope</th>
<th>Information types</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certadm/nf-certadm-iocspadmin-get_ocspserviceproperties">OCSPServiceProperties</a>
</td>
<td>Governs general responder-service behavior for every CA.</td>
<td>
<ul>
<li>Proxy</li>
<li>Audit</li>
<li>Security configurations</li>
</ul>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certadm/nf-certadm-iocspadmin-get_ocspcaconfigurationcollection">OCSPCAConfigurationCollection</a>
</td>
<td>Governs response behavior for a specific CA.</td>
<td>
<ul>
<li>CA</li>
<li>Hash algorithm</li>
<li>Certificate signing</li>
<li>Revocation provider configurations</li>
</ul>
</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/certadm/nf-certadm-iocspcaconfiguration-get_providerproperties">ProviderProperties</a>
</td>
<td>Governs behavior of a revocation information provider that is specific to a particular <a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">OCSPCAConfiguration</a>.</td>
<td>
<ul>
<li>Certificate revocation lists (CRLs)</li>
<li>Refresh interval</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
