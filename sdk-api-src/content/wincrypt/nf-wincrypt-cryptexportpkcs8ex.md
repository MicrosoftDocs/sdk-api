---
UID: NF:wincrypt.CryptExportPKCS8Ex
title: CryptExportPKCS8Ex function (wincrypt.h)
author: windows-sdk-content
description: Exports the private key in PKCS #8 format.
old-location: security\cryptexportpkcs8ex.htm
tech.root: SecCrypto
ms.assetid: 82fee86a-8704-4f22-8f11-f89509c5a0aa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CryptExportPKCS8Ex, CryptExportPKCS8Ex function [Security], security.cryptexportpkcs8ex, wincrypt/CryptExportPKCS8Ex
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
req.lib: 
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
 - CryptExportPKCS8Ex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptExportPKCS8Ex function


## -description


<p class="CCE_Message">[The <b>CryptExportPKCS8Ex</b> function is no longer available for use as of Windows Server 2008 and Windows Vista. Instead, use the <a href="https://msdn.microsoft.com/e8bd54b1-946f-4c65-8a86-96f0dbec07ff">PFXExportCertStoreEx</a> function.]

The <b>CryptExportPKCS8Ex</b> function exports the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> in PKCS #8 format.This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Crypt32.dll.


## -parameters




### -param psExportParams [in]

A pointer to a <a href="https://msdn.microsoft.com/5a60c96e-907a-409e-921c-59055452463f">CRYPT_PKCS8_EXPORT_PARAMS</a> structure that contains information about the key to export.


### -param dwFlags [in]

This parameter should be zero if <i>pbPrivateKeyBlob</i> is <b>NULL</b> and 0x8000 otherwise.


### -param pvAuxInfo [in, optional]

This parameter must be <b>NULL</b>.


### -param pbPrivateKeyBlob [out, optional]

A pointer to an 
array of <b>BYTE</b> structures to receive the private key  to be exported. 


The private key will contain the information in a PKCS #8
PrivateKeyInfo <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) type found in the PKCS #8 standard.

For memory allocation purposes, you can get the size of the private key  to be exported by setting this parameter to <b>NULL</b>. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbPrivateKeyBlob [in, out]

A pointer to a <b>DWORD</b> that may contain, on input, the size, in  bytes,  of the memory allocation needed to contain the <i>pbPrivateKeyBlob</i>. If <i>pbPrivateKeyBlob</i> is <b>NULL</b>, this parameter will return the size of the memory allocation needed for a second call to the function. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following error codes are specific to this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNSUPPORTED_TYPE</b></dt>
</dl>
</td>
<td width="60%">
An export function that can be installed or registered could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pbPrivateKeyBlob</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by the <i>pcbPrivateKeyBlob</i> parameter.

</td>
</tr>
</table>
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>   returns an ASN.1 encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



This function is only supported for asymmetric keys.




## -see-also




<a href="https://msdn.microsoft.com/5a60c96e-907a-409e-921c-59055452463f">CRYPT_PKCS8_EXPORT_PARAMS</a>



<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>



<a href="https://msdn.microsoft.com/defd0b23-d9c2-4b28-a6a6-1be7487ae656">CryptExportPKCS8</a>



<a href="https://msdn.microsoft.com/fa3deff9-b4c1-4b63-a59f-738f87e1a409">CryptImportPKCS8</a>
 

 

