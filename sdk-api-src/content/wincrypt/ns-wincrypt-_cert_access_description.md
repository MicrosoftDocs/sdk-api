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

# _CERT_ACCESS_DESCRIPTION structure


## -description


The <b>CERT_ACCESS_DESCRIPTION</b> structure is a member of a 
<a href="https://msdn.microsoft.com/5f4abb15-3057-4d20-a319-550cec45d1f1">CERT_AUTHORITY_INFO_ACCESS</a> structure. It contains one instance of information about how to access information and services for either the subject or the issuer of a certificate that contains either the subject information access or the authority information access extension, respectively. For more information about these certificate extensions, see <a href="http://go.microsoft.com/fwlink/p/?linkid=104367">RFC 3280</a>.


## -struct-fields




### -field pszAccessMethod

Specifies the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the method of access.

The following are currently defined PKIX Access Method OIDs:

<ul>
<li>szOID_PKIX_CA_ISSUERS</li>
<li>szOID_PKIX_CA_REPOSITORY</li>
<li>szOID_PKIX_OCSP</li>
<li>szOID_PKIX_TIME_STAMPING</li>
</ul>
The default provider does not support the szOID_PKIX_TIME_STAMPING method.


### -field AccessLocation


<a href="https://msdn.microsoft.com/1353ef56-cae7-43f2-a31f-2bb3b502450e">CERT_ALT_NAME_ENTRY</a> structure that describes the online status server and the access protocol to obtain current certificate status information for the certificate containing the extension. 




For the szOID_PKIX_OCSP access method, <b>AccessLocation</b> describes the online status server and the access protocol needed to obtain status information about the certificate containing this extension.

For the szOID_PKIX_CA_ISSUERS access method, <b>AccessLocation</b> obtains information on the CAs that issued certificates superior to the CA that issued the certificate containing this extension. The CA issuer's description is intended to aid certificate users in the selection of a certification path that terminates at a point trusted by the certificate user.

For the szOID_PKIX_CA_REPOSITORY method, <b>AccessLocation</b> specifies either the URI, directory name, or email address of the certificate and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) repository for a  subject that is a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA).


## -see-also




<a href="https://msdn.microsoft.com/5f4abb15-3057-4d20-a319-550cec45d1f1">CERT_AUTHORITY_INFO_ACCESS</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=104367">RFC 3280</a>
 

 

