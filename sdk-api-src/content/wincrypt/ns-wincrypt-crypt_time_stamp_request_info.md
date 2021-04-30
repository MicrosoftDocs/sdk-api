---
UID: NS:wincrypt._CRYPT_TIME_STAMP_REQUEST_INFO
title: CRYPT_TIME_STAMP_REQUEST_INFO (wincrypt.h)
description: Used for time stamping.
helpviewer_keywords: ["*PCRYPT_TIME_STAMP_REQUEST_INFO","CRYPT_TIME_STAMP_REQUEST_INFO","CRYPT_TIME_STAMP_REQUEST_INFO structure [Security]","PCRYPT_TIME_STAMP_REQUEST_INFO","PCRYPT_TIME_STAMP_REQUEST_INFO structure pointer [Security]","_crypto2_crypt_time_stamp_request_info","security.crypt_time_stamp_request_info","wincrypt/CRYPT_TIME_STAMP_REQUEST_INFO","wincrypt/PCRYPT_TIME_STAMP_REQUEST_INFO"]
old-location: security\crypt_time_stamp_request_info.htm
tech.root: security
ms.assetid: 876527dd-1ec5-4783-a7ad-20a0e2d2367a
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TIME_STAMP_REQUEST_INFO, CRYPT_TIME_STAMP_REQUEST_INFO, CRYPT_TIME_STAMP_REQUEST_INFO structure [Security], PCRYPT_TIME_STAMP_REQUEST_INFO, PCRYPT_TIME_STAMP_REQUEST_INFO structure pointer [Security], _crypto2_crypt_time_stamp_request_info, security.crypt_time_stamp_request_info, wincrypt/CRYPT_TIME_STAMP_REQUEST_INFO, wincrypt/PCRYPT_TIME_STAMP_REQUEST_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CRYPT_TIME_STAMP_REQUEST_INFO, *PCRYPT_TIME_STAMP_REQUEST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TIME_STAMP_REQUEST_INFO
 - wincrypt/_CRYPT_TIME_STAMP_REQUEST_INFO
 - PCRYPT_TIME_STAMP_REQUEST_INFO
 - wincrypt/PCRYPT_TIME_STAMP_REQUEST_INFO
 - CRYPT_TIME_STAMP_REQUEST_INFO
 - wincrypt/CRYPT_TIME_STAMP_REQUEST_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRYPT_TIME_STAMP_REQUEST_INFO
---

# CRYPT_TIME_STAMP_REQUEST_INFO structure


## -description

The <b>CRYPT_TIME_STAMP_REQUEST_INFO</b> structure is used for time stamping. To add an authenticated attribute when signing an executable file to verify the date and time of the signature, a signed time stamp is requested from a time stamp server. The <b>CRYPT_TIME_STAMP_REQUEST_INFO</b> structure is used to get a time stamp. It contains the signature bits of the material being time stamped in the <b>Content</b> field.

## -struct-fields

### -field pszTimeStampAlgorithm

The <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that specifies the desired format of the time stamp, usually UTC.

### -field pszContentType

The OID of the Content Type of the content, usually DATA.

### -field Content

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_OBJID_BLOB</a> structure that contains the encoded signature bits of the material being time stamped.

### -field cAttribute

The number of elements in the <b>rgAttribute</b> array.

### -field rgAttribute

Array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures, each holding an encoded attribute.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>