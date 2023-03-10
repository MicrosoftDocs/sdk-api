---
UID: NF:certadm.IOCSPCAConfiguration.put_SigningFlags
title: IOCSPCAConfiguration::put_SigningFlags (certadm.h)
description: Gets or sets a combination of flag values. These values specify the management of signing certificates that belong to a certification authority (CA) configuration. (Put)
helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","SigningFlags property","IOCSPCAConfiguration.SigningFlags","IOCSPCAConfiguration.put_SigningFlags","IOCSPCAConfiguration::SigningFlags","IOCSPCAConfiguration::get_SigningFlags","IOCSPCAConfiguration::put_SigningFlags","SigningFlags property [Security]","SigningFlags property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::SigningFlags","certadm/IOCSPCAConfiguration::get_SigningFlags","certadm/IOCSPCAConfiguration::put_SigningFlags","put_SigningFlags","security.iocspcaconfiguration_signingflags_method"]
old-location: security\iocspcaconfiguration_signingflags_method.htm
tech.root: security
ms.assetid: 00575bb5-eb18-44f2-b2a8-f2f2fd361dec
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],SigningFlags property, IOCSPCAConfiguration.SigningFlags, IOCSPCAConfiguration.put_SigningFlags, IOCSPCAConfiguration::SigningFlags, IOCSPCAConfiguration::get_SigningFlags, IOCSPCAConfiguration::put_SigningFlags, SigningFlags property [Security], SigningFlags property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::SigningFlags, certadm/IOCSPCAConfiguration::get_SigningFlags, certadm/IOCSPCAConfiguration::put_SigningFlags, put_SigningFlags, security.iocspcaconfiguration_signingflags_method
req.header: certadm.h
req.include-header: Certserv.h
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
 - IOCSPCAConfiguration::put_SigningFlags
 - certadm/IOCSPCAConfiguration::put_SigningFlags
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
 - IOCSPCAConfiguration.SigningFlags
 - IOCSPCAConfiguration.get_SigningFlags
 - IOCSPCAConfiguration.put_SigningFlags
---

# IOCSPCAConfiguration::put_SigningFlags


## -description

The <b>SigningFlags</b> property gets or sets a combination of flag values. These values specify the management of signing certificates that belong to a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration.

This property is read/write.

## -parameters

## -remarks

The following table lists bit flag values for 
<b>SigningFlags</b>.

<table>
<tr>
<th>Flag constant</th>
<th>Flag value</th>
<th>Description</th>
</tr>
<tr>
<td><b>OCSP_SF_SILENT</b></td>
<td>0x001</td>
<td>Acquire  a private key silently.</td>
</tr>
<tr>
<td><b>OCSP_SF_USE_CACERT</b></td>
<td>				0x002</td>
<td>Use a CA certificate in this configuration for signing an OCSP response. This option is available only if the responder service is installed on the CA computer.</td>
</tr>
<tr>
<td><b>OCSP_SF_ALLOW_SIGNINGCERT_AUTORENEWAL</b></td>
<td>0x004</td>
<td>Enable a responder service to  automatically transition to a renewed signing certificate.</td>
</tr>
<tr>
<td><b>OCSP_SF_FORCE_SIGNINGCERT_ISSUER_ISCA</b></td>
<td>	0x008</td>
<td>Force a delegated signing certificate to be signed by the CA.</td>
</tr>
<tr>
<td><b>OCSP_SF_AUTODISCOVER_SIGNINGCERT</b></td>
<td>				0x010</td>
<td>Automatically discover a delegated signing certificate.</td>
</tr>
<tr>
<td><b>OCSP_SF_MANUAL_ASSIGN_SIGNINGCERT</b></td>
<td>				0x020</td>
<td>Manually assign a signing certificate.</td>
</tr>
<tr>
<td><b>OCSP_SF_RESPONDER_ID_KEYHASH</b></td>
<td>				0x040</td>
<td>A responder ID includes a hash of the public key of the signing certificate (default).</td>
</tr>
<tr>
<td><b>OCSP_SF_RESPONDER_ID_NAME</b></td>
<td>				0x080</td>
<td>A responder ID includes the name of the subject in a signing certificate.</td>
</tr>
<tr>
<td><b>OCSP_SF_ALLOW_NONCE_EXTENSION</b></td>
<td>				0x100</td>
<td>Enable NONCE extension to be processed by a responder service.</td>
</tr>
<tr>
<td><b>OCSP_SF_ALLOW_SIGNINGCERT_AUTOENROLLMENT</b></td>
<td>				0x200</td>
<td>A responder service can enroll for a signing certificate.</td>
</tr>
</table>
 

When setting <b>SigningFlags</b>, you must specify one of the values <b>OCSP_SF_USE_CACERT</b>, <b>OCSP_SF_AUTODISCOVER_SIGNINGCERT</b>, or <b>OCSP_SF_MANUAL_ASSIGN_SIGNINGCERT</b>.

If you specify <b>OCSP_SF_ALLOW_SIGNINGCERT_AUTOENROLLMENT</b>, you must also specify <b>OCSP_SF_AUTODISCOVER_SIGNINGCERT</b>.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
