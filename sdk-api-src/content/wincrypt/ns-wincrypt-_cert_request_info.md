---
UID: NS:wincrypt._CERT_REQUEST_INFO
title: "_CERT_REQUEST_INFO"
author: windows-sdk-content
description: The CERT_REQUEST_INFO structure contains information for a certificate request. The subject, subject public key, and attribute BLOBs are encoded.
old-location: security\cert_request_info.htm
old-project: seccrypto
ms.assetid: 6edeed33-16e1-4295-90e9-769929ab916a
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "*PCERT_REQUEST_INFO, CERT_REQUEST_INFO, CERT_REQUEST_INFO structure [Security], CERT_V1, PCERT_REQUEST_INFO, PCERT_REQUEST_INFO structure pointer [Security], _CERT_REQUEST_INFO, _crypto2_cert_request_info, security.cert_request_info, wincrypt/CERT_REQUEST_INFO, wincrypt/PCERT_REQUEST_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: CERT_REQUEST_INFO, *PCERT_REQUEST_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_REQUEST_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_REQUEST_INFO structure


## -description


The <b>CERT_REQUEST_INFO</b> structure contains information for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. The subject, subject <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>, and <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute BLOBs</a> are encoded.


## -struct-fields




### -field dwVersion

The certificate's version number. Defined version number is shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_V1"></a><a id="cert_v1"></a><dl>
<dt><b>CERT_V1</b></dt>
</dl>
</td>
<td width="60%">
version 1

</td>
</tr>
</table>
 


### -field Subject

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CERT_NAME_BLOB</a> structure that contains the certificate subject's encoded name.


### -field SubjectPublicKeyInfo


<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a> structure containing the encoded public key and its algorithm.


### -field cAttribute

Number of elements in the <b>rgAttribute</b> array.


### -field rgAttribute

A pointer to an array of <a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures, each holding attribute information about the certificate.


## -see-also




<a href="https://msdn.microsoft.com/bab6c147-b7cd-408a-acac-90f05921e065">CERT_PUBLIC_KEY_INFO</a>



<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>



<a href="https://msdn.microsoft.com/ee138918-ed7c-4980-8b18-64004a0dd7df">CryptSignAndEncodeCertificate</a>
 

 

