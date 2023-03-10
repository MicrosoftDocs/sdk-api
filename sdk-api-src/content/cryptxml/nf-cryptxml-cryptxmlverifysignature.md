---
UID: NF:cryptxml.CryptXmlVerifySignature
title: CryptXmlVerifySignature function (cryptxml.h)
description: Performs a cryptographic signature validation of a SignedInfo element.
helpviewer_keywords: ["CRYPT_XML_FLAG_DISABLE_EXTENSIONS","CryptXmlVerifySignature","CryptXmlVerifySignature function [Security]","cryptxml/CryptXmlVerifySignature","security.cryptxmlverifysignature"]
old-location: security\cryptxmlverifysignature.htm
tech.root: security
ms.assetid: 1f8776dc-d91a-4be9-90bf-7d36d587ffb2
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_FLAG_DISABLE_EXTENSIONS, CryptXmlVerifySignature, CryptXmlVerifySignature function [Security], cryptxml/CryptXmlVerifySignature, security.cryptxmlverifysignature
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptXmlVerifySignature
 - cryptxml/CryptXmlVerifySignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlVerifySignature
---

# CryptXmlVerifySignature function


## -description

The <b>CryptXmlVerifySignature</b> function performs a cryptographic signature 
 validation of a <b>SignedInfo</b> element.

## -parameters

### -param hSignature [in]

The handle of a <b>Signature</b> element.

### -param hKey [in, optional]

The handle of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> to use to verify the signature value on 
    the <b>SignedInfo</b> element.
    This parameter must be <b>NULL</b> for HMAC-based signature algorithms.

### -param dwFlags

A <b>DWORD</b> value that controls which implementations are used. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_XML_FLAG_DISABLE_EXTENSIONS"></a><a id="crypt_xml_flag_disable_extensions"></a><dl>
<dt><b>CRYPT_XML_FLAG_DISABLE_EXTENSIONS</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Only default implementations for the signature and digest are used. When this flag is set, no other registered extensions are loaded.

</td>
</tr>
</table>

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.