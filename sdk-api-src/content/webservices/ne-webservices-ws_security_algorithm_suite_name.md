---
UID: NE:webservices.WS_SECURITY_ALGORITHM_SUITE_NAME
title: WS_SECURITY_ALGORITHM_SUITE_NAME
author: windows-sdk-content
description: A suite of security algorithms used for tasks such as signing and encryting. The values in this enumeration correspond to the suites defined in WS-SecurityPolicy 1.1 section 7.1.
old-location: wsw\ws_security_algorithm_suite_name.htm
old-project: wsw
ms.assetid: cd7116d2-86f6-475e-a55d-050c7e02172d
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_SECURITY_ALGORITHM_SUITE_NAME, WS_SECURITY_ALGORITHM_SUITE_NAME enumeration [Web Services for Windows], WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256, WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256, webservices/WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15, wsw.ws_security_algorithm_suite_name
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: webservices.h
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
req.typenames: WS_SECURITY_ALGORITHM_SUITE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_SECURITY_ALGORITHM_SUITE_NAME
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SECURITY_ALGORITHM_SUITE_NAME enumeration


## -description



        A suite of security algorithms used for tasks such as signing and encryting. 
        The values in this enumeration correspond to the suites defined in 
        WS-SecurityPolicy 1.1
        section 7.1.
      


## -enum-fields




### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256


            Identifies the Basic256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>
            The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192


            Identifies the Basic192 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>
            The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128


            Identifies the Basic128 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>
            The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_RSA15


            Identifies the Basic256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>
            The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_RSA15


            Identifies the Basic192Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>
            The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_RSA15


            Identifies the Basic128RSA15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>
            The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256


            Identifies the Basic256Sha256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>
            The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256


            Identifies the Basic192Sha256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>
            The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256


            Identifies the Basic128Sha256 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_OAEP</a>
</li>
</ul>
            The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256_SHA256_RSA15


            Identifies the Basic256Sha256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>
            The minimum symmetric key length is 256; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC192_SHA256_RSA15


            Identifies the Basic192Sha256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>
            The minimum symmetric key length is 192; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        


### -field WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128_SHA256_RSA15


            Identifies the Basic128Sha256Rsa15 algorithm suite. This suite uses the following algorithms:
            <ul>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_CANONICALIZATION_EXCLUSIVE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_DIGEST_SHA_256</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_SYMMETRIC_SIGNATURE_HMAC_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_SIGNATURE_RSA_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_KEY_DERIVATION_P_SHA1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e1af7178-0671-45d9-9e25-0931b895ad40">WS_SECURITY_ALGORITHM_ASYMMETRIC_KEYWRAP_RSA_1_5</a>
</li>
</ul>
            The minimum symmetric key length is 128; the maximum symmetric key length is 256.
            The minimum asymmetric key length is 1024; the maximum asymmetric key length is 4096.
        

