---
UID: NS:wincrypt._CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
title: "_CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO"
author: windows-driver-content
description: Contains optional extra information that can be passed to the CryptGetTimeValidObject function in the pExtraInfo parameter.
old-location: security\crypt_get_time_valid_object_extra_info.htm
old-project: SecCrypto
ms.assetid: 3de595f9-c922-4c8f-8328-819e91a2997c
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure [Security], PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure pointer [Security], _CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, security.crypt_get_time_valid_object_extra_info, wincrypt/CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, wincrypt/PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO, *PCRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO structure


## -description


 The <b>CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO</b> structure contains optional extra information that can be passed to the <a href="https://msdn.microsoft.com/dd639b43-1560-4e9f-a778-9e20484ae012">CryptGetTimeValidObject</a> function in the <i>pExtraInfo</i> parameter.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field iDeltaCrlIndicator

A value used to compare to the base <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) number. If the base CRL number is less than this value, the caller should attempt to retrieve a newer base CRL.

If the <b>pDeltaCrlIndicator</b> member is non-<b>NULL</b>  the value of this member must be 0x7fffffff.<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Because the <b>pDeltaCrlIndicator</b> member does not exist, the  <b>iDeltaCrlIndicator</b> value requirement does not apply.




### -field pftCacheResync

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that governs the use of cached information. Any information cached  before this time is considered invalid and new information is retrieved.


### -field pLastSyncTime

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that contains the time of the last synchronization of the data retrieved for the object.


### -field pMaxAgeTime

A pointer to a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure that specifies an expiration time of the data retrieved based on the <b>dwMaxAge</b> member of the <a href="https://msdn.microsoft.com/26cd6065-8be9-4b3b-8207-5ad620e9b537">CRYPTNET_URL_CACHE_RESPONSE_INFO</a> structure.


### -field pChainPara

A pointer to a <a href="https://msdn.microsoft.com/9cdcc81a-aef1-4a1e-94f8-7aa461225dae">CERT_REVOCATION_CHAIN_PARA</a> structure that contains the <a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a> function parameters used by the caller. The data in this member enables independent <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) signer certificate chain verification.


### -field pDeltaCrlIndicator

A pointer to a <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains a CRL with a length of more than 4 bytes. If this member is  non-<b>NULL</b> and the <b>iDeltaCrlIndicator</b> member is equal to <b>MAXLONG</b>, then if the base CRL number is less than this value, the caller should attempt to retrieve a newer base CRL.


<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not supported.




## -remarks



All members of the <b>CRYPT_GET_TIME_VALID_OBJECT_EXTRA_INFO</b> structure that do not have a value must be set to zero.



