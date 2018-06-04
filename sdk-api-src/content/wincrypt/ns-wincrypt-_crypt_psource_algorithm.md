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

# _CRYPT_PSOURCE_ALGORITHM structure


## -description


The <b>CRYPT_PSOURCE_ALGORITHM</b> structure identifies the algorithm and (optionally) the value of the label for an RSAES-OAEP key encryption.


## -struct-fields




### -field pszObjId

The address of a null-terminated ANSI string that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the algorithm. This can be the following value or any other mask generation function OID.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_RSA_PSPECIFIED"></a><a id="szoid_rsa_pspecified"></a><a id="SZOID_RSA_PSPECIFIED"></a><dl>
<dt><b>szOID_RSA_PSPECIFIED</b></dt>
<dt>"1.2.840.113549.1.1.9"</dt>
</dl>
</td>
<td width="60%">
The RSAES-OAEP label function.

</td>
</tr>
</table>
 


### -field EncodingParameters

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> that contains the label. This member is optional and may contain an empty BLOB.


## -see-also




<a href="https://msdn.microsoft.com/ebcd25a2-2547-4949-85fd-be5f6c5bfcd2">CRYPT_RSAES_OAEP_PARAMETERS</a>
 

 

