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

# CertAddEncodedCertificateToSystemStoreA function


## -description


The <b>CertAddEncodedCertificateToSystemStore</b> function opens the specified system store and adds the encoded certificate to it.


## -parameters




### -param szCertStoreName [in]

A null-terminated string that contains the name of the system store for the encoded certificate.


### -param pbCertEncoded [in]

A pointer to a buffer that contains the encoded certificate to add.


### -param cbCertEncoded [in]

The size, in bytes, of the <i>pbCertEncoded</i> buffer.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. <b>CertAddEncodedCertificateToSystemStore</b> depends on the functions listed in the following remarks for error handling. Refer to those function topics for their respective error handling behaviors. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Internally, <b>CertAddEncodedCertificateToSystemStore</b> calls <a href="https://msdn.microsoft.com/23699439-1a6c-4907-93fa-651024856be7">CertOpenSystemStore</a> and <a href="https://msdn.microsoft.com/7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d">CertAddEncodedCertificateToStore</a> with the following parameters.


<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/23699439-1a6c-4907-93fa-651024856be7">CertOpenSystemStore</a> Parameter</th>
<th>Value</th>
</tr>
<tr>
<td><i>szSubsystemProtocol</i></td>
<td><i>szCertStoreName</i></td>
</tr>
</table>
 



If <b>CertAddEncodedCertificateToSystemStore</b> obtains a handle to the specified system store, it calls <a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a> to close the handle before it returns.


<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d">CertAddEncodedCertificateToStore</a> Parameter</th>
<th>Value</th>
</tr>
<tr>
<td><i>dwCertEncodingType</i></td>
<td><b>X509_ASN_ENCODING</b></td>
</tr>
<tr>
<td><i>dwAddDisposition</i></td>
<td><b>CERT_STORE_ADD_USE_EXISTING</b></td>
</tr>
<tr>
<td><i>ppCertContext</i></td>
<td><b>NULL</b></td>
</tr>
</table>
 





