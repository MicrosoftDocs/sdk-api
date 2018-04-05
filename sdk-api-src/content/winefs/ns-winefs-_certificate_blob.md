---
UID: NS:winefs._CERTIFICATE_BLOB
title: "_CERTIFICATE_BLOB"
author: windows-driver-content
description: Contains a certificate.
old-location: fs\efs_certificate_blob_str.htm
old-project: FileIO
ms.assetid: e0d0aa0a-ac87-4734-93d0-30c2080319e8
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PEFS_CERTIFICATE_BLOB, CRYPT_ASN_ENCODING, CRYPT_NDR_ENCODING, EFS_CERTIFICATE_BLOB, EFS_CERTIFICATE_BLOB structure [Files], PEFS_CERTIFICATE_BLOB, PEFS_CERTIFICATE_BLOB structure pointer [Files], X509_ASN_ENCODING, X509_NDR_ENCODING, _CERTIFICATE_BLOB, _win32_efs_certificate_blob_str, base.efs_certificate_blob_str, fs.efs_certificate_blob_str, winefs/EFS_CERTIFICATE_BLOB, winefs/PEFS_CERTIFICATE_BLOB"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: EFS_CERTIFICATE_BLOB, *PEFS_CERTIFICATE_BLOB
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winefs.h
api_name:
-	EFS_CERTIFICATE_BLOB
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERTIFICATE_BLOB structure


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


### -field pbData

The binary certificate. The  
      <b>dwCertEncodingType</b> member specifies the format for this certificate.
     


## -see-also




<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>
 

 

