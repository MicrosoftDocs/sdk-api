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

# _CERT_OR_CRL_BLOB structure


## -description


The <b>CERT_OR_CRL_BLOB</b> structure encapsulates certificates for use with Internet Key Exchange messages.


## -struct-fields




### -field dwChoice

A <b>DWORD</b> value that specifies the content type of the buffer pointed to by the <b>pbEncoded</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_BUNDLE_CERTIFICATE"></a><a id="cert_bundle_certificate"></a><dl>
<dt><b>CERT_BUNDLE_CERTIFICATE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The <b>pbEncoded</b> member points to an encoded certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_BUNDLE_CRL"></a><a id="cert_bundle_crl"></a><dl>
<dt><b>CERT_BUNDLE_CRL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <b>pbEncoded</b> member points to a certificate list.

</td>
</tr>
</table>
 


### -field cbEncoded

The size, in bytes, of the buffer pointed to by the <b>pbEncoded</b> member.


### -field pbEncoded

A pointer to a buffer that contains a certificate or a <a href="https://msdn.microsoft.com/a06e71b4-63c7-4d4a-820c-e5901015aaa6">CERT_OR_CRL_BUNDLE</a> structure that contains an array of certificates as specified by the <b>dwChoice</b> member. 

