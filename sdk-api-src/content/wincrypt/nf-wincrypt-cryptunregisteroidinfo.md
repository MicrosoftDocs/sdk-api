---
UID: NF:wincrypt.CryptUnregisterOIDInfo
title: CryptUnregisterOIDInfo function
author: windows-sdk-content
description: The CryptUnregisterOIDInfo function removes the registration of a specified CRYPT_OID_INFO OID information structure. The structure to be unregistered is identified by the structure's pszOID and dwGroupId members.
old-location: security\cryptunregisteroidinfo.htm
old-project: SecCrypto
ms.assetid: 1217397b-2af9-4f58-8616-5a18ee2f4b8c
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CryptUnregisterOIDInfo, CryptUnregisterOIDInfo function [Security], _crypto2_cryptunregisteroidinfo, security.cryptunregisteroidinfo, wincrypt/CryptUnregisterOIDInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptUnregisterOIDInfo
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CryptUnregisterOIDInfo function


## -description


The <b>CryptUnregisterOIDInfo</b> function removes the registration of a specified 
<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a> OID information structure. The structure to be unregistered is identified by the structure's <b>pszOID</b> and <b>dwGroupId</b> members.


## -parameters




### -param pInfo [in]

Specifies the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) information for which the registration is to be removed. The group that the registration is removed for is specified by the <b>dwGroupId</b> member in the <i>pInfo</i>.


## -returns



If the function succeeds, the return value is nonzero (TRUE).

If the function fails, the return value is zero (FALSE).




## -see-also




<a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a>



<a href="https://msdn.microsoft.com/ef0d3aa6-6b36-426f-a14c-2fdf7543deb9">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="https://msdn.microsoft.com/06ba0f60-778d-450b-8f71-23471b8c4e2c">CRYPT_OID_INFO</a>



<a href="https://msdn.microsoft.com/87acf207-d109-4173-9530-8cbbebb473b2">CryptFindOIDInfo</a>



<a href="https://msdn.microsoft.com/7a5b4800-3182-4cd4-b17a-c6d4e11f7047">CryptRegisterOIDInfo</a>



<a href="cryptography_functions.htm">OID Support Functions</a>
 

 

