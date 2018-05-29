---
UID: NF:wincrypt.CryptVerifyTimeStampSignature
title: CryptVerifyTimeStampSignature function
author: windows-sdk-content
description: Validates the time stamp signature on a specified array of bytes.
old-location: security\cryptverifytimestampsignature.htm
old-project: SecCrypto
ms.assetid: 791b1500-98e3-49d5-97aa-be91f5edb7c2
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: CryptVerifyTimeStampSignature, CryptVerifyTimeStampSignature function [Security], security.cryptverifytimestampsignature, wincrypt/CryptVerifyTimeStampSignature
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CryptVerifyTimeStampSignature
product: Windows
targetos: Windows
req.lib: 
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptVerifyTimeStampSignature function


## -description


The <b>CryptVerifyTimeStampSignature</b> function validates the time stamp signature on a specified array of bytes.


## -parameters




### -param pbTSContentInfo [in]

A pointer to a buffer that contains time stamp content.


### -param cbTSContentInfo

The size, in bytes, of the buffer pointed to by the <i>pbTSContentInfo</i> parameter.


### -param pbData [in, optional]

A pointer to an array of bytes on which to validate the time stamp signature.


### -param cbData

The size, in bytes, of the array pointed to by the <i>pbData</i> parameter.


### -param hAdditionalStore [in, optional]

The handle of an additional store to search for supporting
Time Stamping Authority (TSA) signing certificates and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust lists</a> (CTLs).
    This parameter can be <b>NULL</b> if no additional store is to be searched.


### -param ppTsContext [out]

A pointer to a <a href="https://msdn.microsoft.com/2831b2a9-0f84-4e41-a666-5903fc882965">PCRYPT_TIMESTAMP_CONTEXT</a> structure. When you have finished using the context, you must free it by calling the <a href="https://msdn.microsoft.com/fb5c10ba-da8e-4a34-9302-67586a0a9624">CryptMemFree</a> function.


### -param ppTsSigner [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCERT_CONTEXT</a> that
receives the certificate of the signer.
     When you have finished using this structure, you must free it by passing this
pointer to the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function.

Set this parameter to <b>NULL</b> if the TSA signer's certificate is not needed.


### -param phStore [out, optional]

A pointer to a handle that receives the certificate store opened  on CMS to search for supporting certificates.

This parameter can be <b>NULL</b> if the TSA supporting certificates are not needed. When you have finished using this handle,  you  must release it by passing it to  the <a href="https://msdn.microsoft.com/a93fdd65-359e-4046-910d-347c3af01280">CertCloseStore</a> function.


## -returns



If the function succeeds, the function returns <b>TRUE</b>. For extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. 




## -remarks



The caller should validate the <b>pszTSAPolicyId</b> member of the <a href="https://msdn.microsoft.com/05ca0877-5e9d-4b21-9fca-a1eef2cb4626">CRYPT_TIMESTAMP_INFO</a> structure when it is returned by the   <a href="https://msdn.microsoft.com/68ba3d40-08b0-4261-ab2f-6deb1795f830">CryptRetrieveTimeStamp</a> function. If a TSA policy was specified in the request 
     and the <b>ftTime</b> member contains a valid value, the caller should build a certificate context chain with which to populate the <i>ppTsSigner</i> parameter and validate the trust.




## -see-also




<a href="https://msdn.microsoft.com/68ba3d40-08b0-4261-ab2f-6deb1795f830">CryptRetrieveTimeStamp</a>
 

 

