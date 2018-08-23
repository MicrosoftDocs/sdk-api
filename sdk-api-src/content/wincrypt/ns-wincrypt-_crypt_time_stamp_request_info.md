---
UID: NS:wincrypt._CRYPT_TIME_STAMP_REQUEST_INFO
title: "_CRYPT_TIME_STAMP_REQUEST_INFO"
author: windows-sdk-content
description: Used for time stamping.
old-location: security\crypt_time_stamp_request_info.htm
old-project: SecCrypto
ms.assetid: 876527dd-1ec5-4783-a7ad-20a0e2d2367a
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PCRYPT_TIME_STAMP_REQUEST_INFO, CRYPT_TIME_STAMP_REQUEST_INFO, CRYPT_TIME_STAMP_REQUEST_INFO structure [Security], PCRYPT_TIME_STAMP_REQUEST_INFO, PCRYPT_TIME_STAMP_REQUEST_INFO structure pointer [Security], _CRYPT_TIME_STAMP_REQUEST_INFO, _crypto2_crypt_time_stamp_request_info, security.crypt_time_stamp_request_info, wincrypt/CRYPT_TIME_STAMP_REQUEST_INFO, wincrypt/PCRYPT_TIME_STAMP_REQUEST_INFO"
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
req.typenames: CRYPT_TIME_STAMP_REQUEST_INFO, *PCRYPT_TIME_STAMP_REQUEST_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_TIME_STAMP_REQUEST_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CRYPT_TIME_STAMP_REQUEST_INFO structure


## -description


The <b>CRYPT_TIME_STAMP_REQUEST_INFO</b> structure is used for time stamping. To add an authenticated attribute when signing an executable file to verify the date and time of the signature, a signed time stamp is requested from a time stamp server. The <b>CRYPT_TIME_STAMP_REQUEST_INFO</b> structure is used to get a time stamp. It contains the signature bits of the material being time stamped in the <b>Content</b> field.


## -struct-fields




### -field pszTimeStampAlgorithm

The <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) that specifies the desired format of the time stamp, usually UTC.


### -field pszContentType

The OID of the Content Type of the content, usually DATA.


### -field Content

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_OBJID_BLOB</a> structure that contains the encoded signature bits of the material being time stamped.


### -field cAttribute

The number of elements in the <b>rgAttribute</b> array.
					


### -field rgAttribute

Array of pointers to 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> structures, each holding an encoded attribute.


## -see-also




<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a>



<a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a>
 

 

