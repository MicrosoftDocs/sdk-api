---
UID: NS:winefs._CERTIFICATE_BLOB
title: EFS_CERTIFICATE_BLOB (winefs.h)
description: Contains a certificate.
helpviewer_keywords: ["*PEFS_CERTIFICATE_BLOB","CRYPT_ASN_ENCODING","CRYPT_NDR_ENCODING","EFS_CERTIFICATE_BLOB","EFS_CERTIFICATE_BLOB structure [Files]","PEFS_CERTIFICATE_BLOB","PEFS_CERTIFICATE_BLOB structure pointer [Files]","X509_ASN_ENCODING","X509_NDR_ENCODING","_win32_efs_certificate_blob_str","base.efs_certificate_blob_str","fs.efs_certificate_blob_str","winefs/EFS_CERTIFICATE_BLOB","winefs/PEFS_CERTIFICATE_BLOB"]
old-location: fs\efs_certificate_blob_str.htm
tech.root: fs
ms.assetid: e0d0aa0a-ac87-4734-93d0-30c2080319e8
ms.date: 12/05/2018
ms.keywords: '*PEFS_CERTIFICATE_BLOB, CRYPT_ASN_ENCODING, CRYPT_NDR_ENCODING, EFS_CERTIFICATE_BLOB, EFS_CERTIFICATE_BLOB structure [Files], PEFS_CERTIFICATE_BLOB, PEFS_CERTIFICATE_BLOB structure pointer [Files], X509_ASN_ENCODING, X509_NDR_ENCODING, _win32_efs_certificate_blob_str, base.efs_certificate_blob_str, fs.efs_certificate_blob_str, winefs/EFS_CERTIFICATE_BLOB, winefs/PEFS_CERTIFICATE_BLOB'
req.header: winefs.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional [desktop apps only]
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
req.typenames: EFS_CERTIFICATE_BLOB, *PEFS_CERTIFICATE_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERTIFICATE_BLOB
 - winefs/_CERTIFICATE_BLOB
 - PEFS_CERTIFICATE_BLOB
 - winefs/PEFS_CERTIFICATE_BLOB
 - EFS_CERTIFICATE_BLOB
 - winefs/EFS_CERTIFICATE_BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winefs.h
api_name:
 - EFS_CERTIFICATE_BLOB
---

# EFS_CERTIFICATE_BLOB structure


## -description

Contains a certificate.

## -struct-fields

### -field dwCertEncodingType

A certificate encoding type. This member can be one of the following values.

<a id="CRYPT_ASN_ENCODING"></a>
<a id="crypt_asn_encoding"></a>


#### CRYPT_ASN_ENCODING

<a id="CRYPT_NDR_ENCODING"></a>
<a id="crypt_ndr_encoding"></a>


#### CRYPT_NDR_ENCODING

<a id="X509_ASN_ENCODING"></a>
<a id="x509_asn_encoding"></a>


#### X509_ASN_ENCODING

<a id="X509_NDR_ENCODING"></a>
<a id="x509_ndr_encoding"></a>


#### X509_NDR_ENCODING

### -field cbData

The number of bytes in the <b>pbData</b> buffer.

### -field cbData.range

### -field cbData.range.0

### -field cbData.range.32768

### -field pbData

The binary certificate. The  
      <b>dwCertEncodingType</b> member specifies the format for this certificate.

### -field pbData.size_is

### -field pbData.size_is.cbData

## -see-also

<a href="/windows/desktop/api/winefs/ns-winefs-encryption_certificate">ENCRYPTION_CERTIFICATE</a>



<a href="/windows/desktop/FileIO/file-encryption">File Encryption</a>