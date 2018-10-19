---
UID: NF:wincrypt.CertAlgIdToOID
title: CertAlgIdToOID function
author: windows-sdk-content
description: Converts a CryptoAPI algorithm identifier (ALG_ID) to an Abstract Syntax Notation One (ASN.1) object identifier (OID) string.
old-location: security\certalgidtooid.htm
tech.root: seccrypto
ms.assetid: 2a66c6da-22dd-4192-9f3d-2fb85f8032e0
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CertAlgIdToOID, CertAlgIdToOID function [Security], _crypto2_certalgidtooid, security.certalgidtooid, wincrypt/CertAlgIdToOID
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
 - CertAlgIdToOID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertAlgIdToOID function


## -description


Use the <a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a> function instead of this function because <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> identifiers are no longer supported in CNG. Use the <b>CRYPT_OID_INFO_CNG_ALGID_KEY</b> value in the <i>dwKeyType</i> parameter of the <a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a> function instead.

<b>Windows Server 2003 and Windows XP:  </b>The <b>CertAlgIdToOID</b> function converts a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CryptoAPI</a> algorithm identifier (<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>) to an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) string.




## -parameters




### -param dwAlgId [in]

Value to be converted to an OID.


## -returns



If the function succeeds, the function returns the null-terminated OID string.

If no OID string corresponds to the algorithm identifier, the function returns <b>NULL</b>.




## -see-also




<a href="cryptography_functions.htm">Data Conversion Functions</a>
 

 

