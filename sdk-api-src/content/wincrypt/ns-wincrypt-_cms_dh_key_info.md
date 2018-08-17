---
UID: NS:wincrypt._CMS_DH_KEY_INFO
title: "_CMS_DH_KEY_INFO"
author: windows-sdk-content
description: Used with the KP_CMS_DH_KEY_INFO parameter in the CryptSetKeyParam function to contain Diffie-Hellman key information.
old-location: security\cms_dh_key_info.htm
old-project: SecCrypto
ms.assetid: ecfd8a63-95f9-4026-b31b-671ea58b683f
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: "*PCMS_DH_KEY_INFO, CMS_DH_KEY_INFO, CMS_DH_KEY_INFO structure [Security], PCMS_DH_KEY_INFO, PCMS_DH_KEY_INFO structure pointer [Security], _CMS_DH_KEY_INFO, security.cms_dh_key_info, wincrypt/CMS_DH_KEY_INFO, wincrypt/PCMS_DH_KEY_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: CMS_DH_KEY_INFO, *PCMS_DH_KEY_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMS_DH_KEY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMS_DH_KEY_INFO structure


## -description


The <b>CMS_DH_KEY_INFO</b> structure is used with the <b>KP_CMS_DH_KEY_INFO</b> parameter in the <a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a> function to contain <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Diffie-Hellman</a> key information.


## -struct-fields




### -field dwVersion

The size, in bytes, of this structure.


### -field Algid

One of the <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> values that identifies the algorithm for the key to be converted.


### -field pszContentEncObjId

The address of a null-terminated ANSI string that contains the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) of the content encryption algorithm.


### -field PubInfo

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure that contains additional public information. This member is optional and the <b>cbData</b> member of this structure can be zero if this is not needed.


### -field pReserved

Reserved for future use and must be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/e99a84a2-c23e-4251-8062-dd286ccc29b7">CryptSetKeyParam</a>
 

 

