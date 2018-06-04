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
        

