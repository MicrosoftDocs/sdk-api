---
UID: NS:wincrypt._CRYPT_TIMESTAMP_INFO
title: "_CRYPT_TIMESTAMP_INFO"
author: windows-sdk-content
description: Contains a signed data content type in Cryptographic Message Syntax (CMS) format.
old-location: security\crypt_timestamp_info.htm
old-project: SecCrypto
ms.assetid: 05ca0877-5e9d-4b21-9fca-a1eef2cb4626
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCRYPT_TIMESTAMP_INFO, CRYPT_TIMESTAMP_INFO, CRYPT_TIMESTAMP_INFO structure [Security], PCRYPT_TIMESTAMP_INFO, PCRYPT_TIMESTAMP_INFO structure pointer [Security], TIMESTAMP_VERSION, _CRYPT_TIMESTAMP_INFO, security.crypt_timestamp_info, wincrypt/CRYPT_TIMESTAMP_INFO, wincrypt/PCRYPT_TIMESTAMP_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CRYPT_TIMESTAMP_INFO, *PCRYPT_TIMESTAMP_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CRYPT_TIMESTAMP_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_TIMESTAMP_INFO structure


## -description


The <b>CRYPT_TIMESTAMP_INFO</b> structure contains a signed data content type in Cryptographic Message Syntax (CMS) format.


## -struct-fields




### -field dwVersion

A <b>DWORD</b> value that specifies the version of the time stamp request.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIMESTAMP_VERSION"></a><a id="timestamp_version"></a><dl>
<dt><b>TIMESTAMP_VERSION</b></dt>
<dt>	1</dt>
</dl>
</td>
<td width="60%">
Specifies that this is a version 1 time stamp request.

</td>
</tr>
</table>
 


### -field pszTSAPolicyId

Optional. A pointer to a null-terminated string that specifies the Time Stamping Authority (TSA) policy under which the time stamp token was provided. This value must correspond with the value passed  in the <a href="https://msdn.microsoft.com/1576986c-1a9b-4fcf-9dab-987b472a8671">CRYPT_TIMESTAMP_REQUEST</a> structure.


### -field HashAlgorithm

A <a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains information about the algorithm used to calculate the hash. This value must correspond with the value passed  in the <a href="https://msdn.microsoft.com/1576986c-1a9b-4fcf-9dab-987b472a8671">CRYPT_TIMESTAMP_REQUEST</a> structure.


### -field HashedMessage

A <a href="https://msdn.microsoft.com/1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f">CRYPT_DER_BLOB</a> structure that specifies the hash values to be time stamped.


### -field SerialNumber

 A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the serial number assigned by the TSA to each time stamp token.


### -field ftTime

A <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> value that specifies the time at which the time stamp token was produced by the TSA.


### -field pvAccuracy

Optional. A pointer to a <a href="https://msdn.microsoft.com/9115db8a-7cc1-4360-b89b-6c33ddb67fe9">CRYPT_TIMESTAMP_ACCURACY</a>   structure that contains the time deviation around the UTC time at which the time stamp token was created by the TSA.


### -field fOrdering

This member is reserved.


### -field Nonce

Optional. A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure that contains the nonce value used by the client to verify the
timeliness of the response when no local clock is available. This value must correspond with the value passed  in the <a href="https://msdn.microsoft.com/1576986c-1a9b-4fcf-9dab-987b472a8671">CRYPT_TIMESTAMP_REQUEST</a> structure.


### -field Tsa

Optional. A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DER_BLOB</a> structure that contains the subject name of the TSA certificate.


### -field cExtension

The number of elements in the array pointed to by the <b>rgExtension</b> member.


### -field rgExtension

A pointer to an array of <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structures that contain extension information returned from the request.

