---
UID: NF:cryptxml.CryptXmlGetSignature
title: CryptXmlGetSignature function (cryptxml.h)
description: Returns an XML Signature element.
helpviewer_keywords: ["CryptXmlGetSignature","CryptXmlGetSignature function [Security]","cryptxml/CryptXmlGetSignature","security.cryptxmlgetsignature"]
old-location: security\cryptxmlgetsignature.htm
tech.root: security
ms.assetid: ef6748eb-1d3b-43e0-9525-2b588c2ae13f
ms.date: 12/05/2018
ms.keywords: CryptXmlGetSignature, CryptXmlGetSignature function [Security], cryptxml/CryptXmlGetSignature, security.cryptxmlgetsignature
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
 - CryptXmlGetSignature
 - cryptxml/CryptXmlGetSignature
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
 - CryptXmlGetSignature
---

# CryptXmlGetSignature function


## -description

The <b>CryptXmlGetSignature</b> function returns an XML <b>Signature</b> element.

## -parameters

### -param hCryptXml [in]

The handle of the <b>Signature</b> element.

### -param ppStruct [out]

A pointer to a  pointer to a <a href="/windows/desktop/api/cryptxml/ns-cryptxml-crypt_xml_signature">CRYPT_XML_SIGNATURE</a> structure to receive the signature.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.