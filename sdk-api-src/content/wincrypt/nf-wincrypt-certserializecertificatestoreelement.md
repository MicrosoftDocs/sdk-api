---
UID: NF:wincrypt.CertSerializeCertificateStoreElement
title: CertSerializeCertificateStoreElement function
author: windows-sdk-content
description: The CertSerializeCertificateStoreElement function serializes a certificate context's encoded certificate and its encoded properties. The result can be persisted to storage so that the certificate and properties can be retrieved at a later time.
old-location: security\certserializecertificatestoreelement.htm
old-project: seccrypto
ms.assetid: 104fc986-6344-41b7-8843-23c3c72405a2
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CertSerializeCertificateStoreElement, CertSerializeCertificateStoreElement function [Security], _crypto2_certserializecertificatestoreelement, security.certserializecertificatestoreelement, wincrypt/CertSerializeCertificateStoreElement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - CertSerializeCertificateStoreElement
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertSerializeCertificateStoreElement function


## -description



			The <b>CertSerializeCertificateStoreElement</b> function serializes a certificate context's encoded certificate and its encoded properties. The result can be persisted to storage so that the certificate and properties can be retrieved at a later time.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> to be serialized.


### -param dwFlags [in]

Reserved for future use and must be zero.


### -param pbElement [out]

A pointer to a buffer that receives the serialized output, including the encoded certificate and possibly its properties. 




This parameter can be <b>NULL</b> to set the size of this information for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbElement [in, out]

A pointer to a <b>DWORD</b> value specifying the size, in bytes, of the buffer pointed to by the <i>pbElement</i> parameter. When the function returns, <b>DWORD</b> value contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns




						If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a>



<a href="https://msdn.microsoft.com/library/Aa380252(v=VS.85).aspx">Certificate Functions</a>
 

 

