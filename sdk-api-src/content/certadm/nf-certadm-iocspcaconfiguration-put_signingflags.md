---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IOCSPCAConfiguration::put_SigningFlags


## -description


The <b>SigningFlags</b> property gets or sets a combination of flag values. These values specify the management of signing certificates that belong to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) configuration.

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




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

