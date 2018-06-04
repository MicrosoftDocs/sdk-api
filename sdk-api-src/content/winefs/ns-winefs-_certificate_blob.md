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


### -field cbData.range

 


### -field cbData.range.0

 


### -field cbData.range.32768

 


### -field pbData

The binary certificate. The  
      <b>dwCertEncodingType</b> member specifies the format for this certificate.
     


### -field pbData.size_is

 


### -field pbData.size_is.cbData

 




## -see-also




<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>
 

 

