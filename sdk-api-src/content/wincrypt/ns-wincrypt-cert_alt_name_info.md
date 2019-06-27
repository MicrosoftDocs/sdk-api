---
UID: NS:wincrypt._CERT_ALT_NAME_INFO
title: CERT_ALT_NAME_INFO (wincrypt.h)
author: windows-sdk-content
description: The CERT_ALT_NAME_INFO structure is used in encoding and decoding extensions for subject or issuer certificates, Certificate Revocation Lists (CRLs), and Certificate Trust Lists (CTLs).
old-location: security\cert_alt_name_info.htm
tech.root: SecCrypto
ms.assetid: f9a20827-3333-4ce2-b074-2e8ce903fad2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCERT_ALT_NAME_INFO, CERT_ALT_NAME_INFO, CERT_ALT_NAME_INFO structure [Security], PCERT_ALT_NAME_INFO, PCERT_ALT_NAME_INFO structure pointer [Security], _crypto2_cert_alt_name_info, security.cert_alt_name_info, wincrypt/CERT_ALT_NAME_INFO, wincrypt/PCERT_ALT_NAME_INFO"
ms.topic: struct
f1_keywords: 
 - "wincrypt/CERT_ALT_NAME_INFO"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_ALT_NAME_INFO
product: Windows
targetos: Windows
req.typenames: CERT_ALT_NAME_INFO, *PCERT_ALT_NAME_INFO
req.redist: 
ms.custom: 19H1
---

# CERT_ALT_NAME_INFO structure


## -description


The <b>CERT_ALT_NAME_INFO</b> structure is used in encoding and decoding extensions for subject or issuer <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificates</a>, <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Revocation Lists</a> (CRLs), and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Trust Lists</a> (CTLs).


<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_extension">CERT_EXTENSION</a> structure's <b>Value</b> member with its structure's <b>pszObjId</b> member set to szOID_SUBJECT_ALT_NAME or szOID_ISSUER_ALT_NAME.

An instance of this structure can be used as input to <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> to create an appropriate <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_extension">CERT_EXTENSION</a>.


## -struct-fields




### -field cAltEntry

Number of elements in the <b>rgAltEntry</b> array.


### -field rgAltEntry

Array of 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> structures.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a>
 

 

