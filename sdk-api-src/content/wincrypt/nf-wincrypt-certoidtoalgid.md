---
UID: NF:wincrypt.CertOIDToAlgId
title: CertOIDToAlgId function
author: windows-sdk-content
description: Use the CryptFindOIDInfo function instead of this function because ALG_ID identifiers are no longer supported in CNG.
old-location: security\certoidtoalgid.htm
tech.root: seccrypto
ms.assetid: 920b2642-ce7c-4098-8720-5a6f24128787
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CertOIDToAlgId, CertOIDToAlgId function [Security], _crypto2_certoidtoalgid, security.certoidtoalgid, wincrypt/CertOIDToAlgId
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertOIDToAlgId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertOIDToAlgId function


## -description


Use the <a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a> function instead of this function because <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> identifiers are no longer supported in CNG. Use the <b>CRYPT_OID_INFO_OID_KEY</b> value in the <i>dwKeyType</i> parameter of the <a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a> function instead.

<b>Windows Server 2003 and Windows XP:  </b>The <b>CertOIDToAlgId</b> function converts the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) string to the CryptoAPI algorithm identifier (<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>).




## -parameters




### -param pszObjId [in]

Pointer to the ASN.1 OID to be converted to an algorithm identifier.


## -returns



Returns the 
<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> that corresponds to the object identifier (OID) or zero if no <b>ALG_ID</b> corresponds to the OID.




## -see-also




<a href="cryptography_functions.htm">Data Conversion Functions</a>
 

 

