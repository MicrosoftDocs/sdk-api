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

# _CRYPT_SMIME_CAPABILITY structure


## -description


The <b>CRYPT_SMIME_CAPABILITY</b> structure specifies a single capability and its associated parameters. Single capabilities are grouped together into a list of 
<a href="https://msdn.microsoft.com/2ee70ff5-4ef4-457c-90c8-629ad0bc3c25">CRYPT_SMIME_CAPABILITIES</a> which can specify a prioritized list of capability preferences.
<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/2ee70ff5-4ef4-457c-90c8-629ad0bc3c25">CRYPT_SMIME_CAPABILITIES</a> is part of an Internet draft proposal. For a complete definition, see "draft-dusse-s/mime-cert-01.txt" dated May 5, 1997.</div><div> </div>

## -struct-fields




### -field pszObjId

<a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">Object identifier</a> (OID) for a capability. Capabilities include signature algorithms, <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">symmetric algorithms</a>, and key enciphering algorithms. Also included are non-algorithm capabilities, which are the preference for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signed data</a> and the preference for unencrypted messages.


### -field Parameters


						A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> structure that contains any parameters associated with the specified capability in <b>pszObjId</b>. 




<div class="alert"><b>Note</b>  For 
<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> and 
<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a> with the <i>dwCertEncodingType</i> set to X509_ASN_ENCODING, if the <b>cbData</b> member of the <b>Parameters</b> member is zero, the encoded parameters are omitted. They are not encoded as a <b>NULL</b> (05 00) as is done when encoding a 
<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>. This follows the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Secure/Multipurpose Internet Mail Extensions</a> (S/MIME) specification for encoding capabilities that requires this omission.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/2ee70ff5-4ef4-457c-90c8-629ad0bc3c25">CRYPT_SMIME_CAPABILITIES</a>
 

 

