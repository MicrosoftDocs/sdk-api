---
UID: NF:cryptxml.CryptXmlImportPublicKey
title: CryptXmlImportPublicKey function (cryptxml.h)
description: Imports the public key specified by the supplied handle.
helpviewer_keywords: ["CRYPT_XML_FLAG_DISABLE_EXTENSIONS","CryptXmlImportPublicKey","CryptXmlImportPublicKey function [Security]","cryptxml/CryptXmlImportPublicKey","security.cryptxmlimportpublickey"]
old-location: security\cryptxmlimportpublickey.htm
tech.root: security
ms.assetid: 599e8bbd-a41f-4781-850d-6590d22d9c3c
ms.date: 12/05/2018
ms.keywords: CRYPT_XML_FLAG_DISABLE_EXTENSIONS, CryptXmlImportPublicKey, CryptXmlImportPublicKey function [Security], cryptxml/CryptXmlImportPublicKey, security.cryptxmlimportpublickey
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
 - CryptXmlImportPublicKey
 - cryptxml/CryptXmlImportPublicKey
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
 - CryptXmlImportPublicKey
---

# CryptXmlImportPublicKey function


## -description

The CryptXmlImportPublicKey function imports the <a href="/windows/desktop/SecGloss/p-gly">public key</a> specified by the supplied handle.

## -parameters

### -param dwFlags

A <b>DWORD</b> value that controls which CryptXML extensions are loaded. This parameter can be one of the following values.


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
Only default implementations for the signature and
digest  are used.  When this flag is set, no other registered extensions are loaded.

</td>
</tr>
</table>

### -param pKeyValue [in]

A pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_key_value">CRYPT_XML_KEY_VALUE</a> structure to receive the imported key.

### -param phKey [out]

A pointer to the handle of the key to import.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.