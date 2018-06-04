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

# _OCSP_BASIC_RESPONSE_ENTRY structure


## -description


The <b>OCSP_BASIC_RESPONSE_ENTRY</b> structure contains the current certificate status for a single certificate. This structure populates the <a href="https://msdn.microsoft.com/f067bfa0-114b-4295-bbee-a963d8b64332">OCSP_BASIC_RESPONSE_INFO</a> <b>rgResponseEntry</b> member.


## -struct-fields




### -field CertId

An <a href="https://msdn.microsoft.com/58717990-a7f7-4b41-aceb-cbce55411396">OCSP_CERT_ID</a> structure that specifies the target certificate of the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) response. 


### -field dwCertStatus

A value that indicates the target certificate revocation status.


<a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560</a> defines the following possible values for certificate status.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OCSP_BASIC_GOOD_CERT_STATUS"></a><a id="ocsp_basic_good_cert_status"></a><dl>
<dt><b>OCSP_BASIC_GOOD_CERT_STATUS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The certificate is not revoked.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_BASIC_REVOKED_CERT_STATUS"></a><a id="ocsp_basic_revoked_cert_status"></a><dl>
<dt><b>OCSP_BASIC_REVOKED_CERT_STATUS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The certificate is revoked either permanently or temporarily.

</td>
</tr>
<tr>
<td width="40%"><a id="OCSP_BASIC_UNKNOWN_CERT_STATUS"></a><a id="ocsp_basic_unknown_cert_status"></a><dl>
<dt><b>OCSP_BASIC_UNKNOWN_CERT_STATUS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The responder has no information for the target certificate.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.pRevokedInfo

A pointer to an <a href="https://msdn.microsoft.com/4475cf2a-bf25-427d-8e53-5e5b96dd676a">OCSP_BASIC_REVOKED_INFO</a> structure that specifies the reason the target certificate was revoked.


### -field ThisUpdate

The date and time at which the response indicated by <i>dwCertStatus</i> is known to be correct.


### -field NextUpdate

The date and time on or before which newer information will be available for the certificate status. A value of zero indicates that the certificate status never expires.


### -field cExtension

The number of elements in the <b>rgExtension</b> array.


### -field rgExtension

An array of pointers to  <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures, each of which contains additional information about the response.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/f067bfa0-114b-4295-bbee-a963d8b64332">OCSP_BASIC_RESPONSE_INFO</a>



<a href="https://msdn.microsoft.com/4475cf2a-bf25-427d-8e53-5e5b96dd676a">OCSP_BASIC_REVOKED_INFO</a>



<a href="https://msdn.microsoft.com/58717990-a7f7-4b41-aceb-cbce55411396">OCSP_CERT_ID</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=91156">RFC 2560 Online Certificate Status Protocol</a>
 

 

