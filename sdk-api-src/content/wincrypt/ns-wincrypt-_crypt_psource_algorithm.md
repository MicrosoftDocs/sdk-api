---
UID: NS:wincrypt._CRYPT_PSOURCE_ALGORITHM
title: "_CRYPT_PSOURCE_ALGORITHM"
author: windows-sdk-content
description: Identifies the algorithm and (optionally) the value of the label for an RSAES-OAEP key encryption.
old-location: security\crypt_psource_algorithm.htm
tech.root: seccrypto
ms.assetid: cd390487-2bba-4d57-a779-579ffbd16acb
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PCRYPT_PSOURCE_ALGORITHM, CRYPT_PSOURCE_ALGORITHM, CRYPT_PSOURCE_ALGORITHM structure [Security], PCRYPT_PSOURCE_ALGORITHM, PCRYPT_PSOURCE_ALGORITHM structure pointer [Security], _CRYPT_PSOURCE_ALGORITHM, security.crypt_psource_algorithm, szOID_RSA_PSPECIFIED, wincrypt/CRYPT_PSOURCE_ALGORITHM, wincrypt/PCRYPT_PSOURCE_ALGORITHM"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_PSOURCE_ALGORITHM
product: Windows
targetos: Windows
req.typenames: CRYPT_PSOURCE_ALGORITHM, *PCRYPT_PSOURCE_ALGORITHM
req.redist: 
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
 

 

